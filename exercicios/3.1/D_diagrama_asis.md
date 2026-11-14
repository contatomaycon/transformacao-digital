# Diagrama AS-IS — jornada do Seguro-Desemprego pela URA CAIXA

**Aluno:** Maycon Douglas — TD-2026-03. **Data:** 14/11/2026.
**Serviço:** Atendimento ao Seguro-Desemprego pela URA da Caixa Econômica
Federal, CAIXA Cidadão 0800 726 0207.

Este diagrama deriva do [blueprint da Parte C](C_blueprint_asis.md) e das
**rodadas 2,5,7,8 e 11 (G02,G05,G07,G08,G11)** do
[transcript](C_grill_transcript.md). É AS-IS documental do caso de 2025,
não teste do canal atual nem redesenho TO-BE.

## Legenda

E1–E8 mantêm os nomes da Parte C. Setas entre etapas mostram sequência e
alternativas; sua presença não significa integração técnica. Relações
tracejadas com atores/recursos mostram suporte e dependências, com **C**
(descrição do caso), **F** (competência publicada), **I** (inferência
funcional) ou **L** (detalhe não levantado). Nenhuma seta representa uma
API comprovada. O fluxo distingue fim de contato de resolução da dúvida.

## Jornada e relações operacionais

```mermaid
flowchart TB
    subgraph JORNADA["Ações do Cidadão e alternativas do contato"]
        E1["E1 Busca informação e liga · F01"]
        E2["E2 Ouve menu e escolhe opção · F01"]
        E3["E3 Informa identificação solicitada · F02"]
        E4["E4 Recebe resposta automática · F03"]
        E5["E5 Solicita pessoa e aguarda · F04"]
        E6["E6 Explica demanda ao atendente · F05/F06"]
        E7["E7 Recebe orientação ou encaminhamento · F07"]
        E8["E8 Encerra, procura destino ou volta a ligar · F07"]
        E1 -->|"contato iniciado, se acessível"| E2
        E2 -->|"opção escolhida"| E3
        E3 -->|"se consegue prosseguir"| E4
        E4 -->|"se encerra após a mensagem"| E8
        E4 -->|"se busca atendimento humano"| E5
        E5 -->|"se obtém atendimento humano"| E6
        E5 -->|"possível interrupção, não resolução comprovada"| E8
        E6 -->|"resultado ou limite da consulta"| E7
        E7 -->|"orientação conclusiva ou inconclusiva"| E8
        E8 -->|"se volta a ligar, nova tentativa"| E1
    end

    subgraph CONTATO["Frontstage: interface percebida"]
        URA["URA CAIXA: menu, solicitação e mensagem"]
        N1F["Atendente N1 falando com o Cidadão"]
        URA -->|"apresenta opções · C"| E2
        URA -->|"solicita identificação · C"| E3
        URA -->|"comunica informação · C"| E4
        N1F -->|"ouve e conversa · C"| E6
        N1F -->|"comunica orientação · C"| E7
    end

    subgraph BASTIDOR["Backstage: ação fora da percepção do cidadão"]
        N1B["Atendente N1 consultando e interpretando"]
        N2["Analista CAIXA N2: retaguarda condicional"]
        N1F -.->|"mesmo papel cruza a Linha de Visibilidade"| N1B
        N1B -.->|"exceção quando aplicável · papel C, fluxo específico L"| N2
        N1B -.->|"consulta disponível, indisponível ou divergente"| E7
    end

    subgraph SUPORTE["Processos e recursos de suporte"]
        TEL["Telefonia e sistema de atendimento · I"]
        FILA["Mecanismo de fila e capacidade · I, plataforma L"]
        DADOS["SISDE/SIISO e informações MTE/Dataprev · C, interface L"]
        GEST["Gestor do serviço CAIXA: função organizacional · I"]
        TEC["Suporte técnico da URA: função técnica · I"]
        TEL -.->|"viabiliza o contato; implementação L"| E1
        FILA -.->|"suporta a espera; algoritmo e SLA L"| E5
        N1B -.->|"consultas relatadas no estudo; acesso vigente L"| DADOS
        GEST -.->|"organização de capacidade; processo vigente L"| FILA
        TEC -.->|"sustentação técnica; prestador L"| TEL
    end

    MTE["MTE: domínio administrativo do benefício"]
    DAT["Dataprev: informação e tecnologia"]
    REDE["Rede SINE/SRTE: possível novo atendimento"]
    DAT -.->|"dependência de informação, sem ligação URA-API comprovada"| MTE
    E8 -->|"se busca canal competente, outra interação"| MTE
    E8 -->|"se procura posto competente, outra interação"| REDE
```

## Correspondência com a Parte C

| Elemento de D | Origem em C | Relação que torna explícita |
| --- | --- | --- |
| E1–E4 e URA | Matriz: entrada, menu, identificação e resposta | A interface automatizada não é o processamento interno nem prova autenticação forte |
| E4 → E8 / E4 → E5 | Saídas condicionais; G07 | Encerrar após mensagem e buscar atendimento humano são alternativas |
| E5 → E6 / E5 → E8 | Espera e possível interrupção | Esperar não garante acesso humano ou resolução da dúvida |
| N1F / N1B / N2 | Frontstage e backstage em E6; G05 | Mesmo N1 cruza a visibilidade; N2 é retaguarda condicional |
| Telefonia, fila e dados | Processos de suporte; G06 | Recursos sustentam ações, com plataforma, interface e acessos desconhecidos |
| E6 → E7 | F05/F06 separados no catálogo | O resultado pode ser informação disponível, limitação ou divergência; não sucesso automático |
| E7 → E8 → E1 | F07 e recontato; G07/G08 | Orientação inconclusiva pode gerar nova tentativa, sem frequência presumida |
| MTE/Dataprev/Rede SINE/SRTE | Competências e fronteira de C | Dependência externa não significa API ou transferência de chamada |

## Fail points conservados

**F01:** barreira de acesso/compreensão em E1/E2; **F02:** identificador
não localizado em E3; **F03:** resposta genérica em E4; **F04:** espera e
possível interrupção em E5; **F05:** informação indisponível em E6;
**F06:** informação divergente em E6; **F07:** encaminhamento inconclusivo
e possível recontato em E7/E8. O catálogo de C fornece fontes e limites.

F05 não produz informação consultada com sucesso; F06 não concede a N1
poder de corrigir dados externos. A interrupção não mede resolução e o
retorno não é obrigatório. Detalhes de identificação, áudio exato,
consulta, registro e continuidade permanecem L. O diagrama não acrescenta
login gov.br, biometria, API unificada, callback ou acompanhamento pactuado.

## Base metodológica e documental

O método é o da aula04.pdf fornecida pelo aluno, páginas PDF 29–32,35,40,
identificada em C. A operação está descrita no
[estudo da disciplina](https://github.com/alexlopespereira/idp_governodigital/blob/main/trabalho_final/seguro-desemprego-ura-caixa.pdf),
páginas PDF 5–6 e 12–15; fronteiras de competência foram confrontadas com
[MTE](https://www.gov.br/pt-br/servicos/solicitar-o-seguro-desemprego) e
[CAIXA](https://www.caixa.gov.br/beneficios-trabalhador/seguro-desemprego/perguntas-frequentes/Paginas/default.aspx).
Todos os nomes, etapas e dependências estão na Parte C e no transcript.
