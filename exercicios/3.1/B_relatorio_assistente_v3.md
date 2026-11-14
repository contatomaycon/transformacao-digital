# Pesquisa final v3 — uma operação condicional, com bastidores e lacunas

A segunda auditoria mudou três aspectos do diagnóstico: explicitou as
saídas alternativas, separou falhas de consulta e tornou visível a barreira
de acesso antes da navegação. Esta versão consolida a base da autoentrevista,
do Service Blueprint AS-IS e do diagrama da jornada.

**Serviço:** Atendimento ao Seguro-Desemprego pela URA CAIXA, CAIXA Cidadão
0800 726 0207. **Autoria:** agente Codex. **Pesquisa:** 14/11/2026.
**Temporalidade:** AS-IS documental do caso com dados de 2025, confrontado
com competências institucionais publicadas; não é teste do canal ao vivo.

## 1. Deltas com gatilho na auditoria 2

| Delta | Gatilho | Alteração de conteúdo | Onde verificar |
| --- | --- | --- | --- |
| D1 | A2-01: saídas agrupadas | A sequência passa a ter saída após autoatendimento, ramo humano opcional e distinção entre conclusão do contato, encaminhamento e recontato | Seção 3: regras de ramificação; não existe retorno obrigatório |
| D2 | A2-02: indisponibilidade e divergência agregadas | F05 e F06 distinguem não obter informação de obter informação incompatível. O antigo F06 de encaminhamento passa a F07 | Seção 5: fatos, efeito percebido e limite de competência separados |
| D3 | A2-03: exclusão antes do menu | F01 passa a alcançar E1/E2. A barreira do menu é C; eventual impedimento anterior à navegação é I, sem contagem observada | Seções 2 e 5: perspectiva do cidadão e grau de evidência |

## 2. Critério de evidência e método

**C** é descrição do caso nas páginas citadas; **F** é informação
institucional/normativa publicada; **I** é inferência funcional; **L** é
detalhe não levantado. Os códigos não tornam toda a operação comprovada.
A aula anexada R1 determina as cinco camadas e três linhas. O estudo R2
documenta a jornada de referência, mas não substitui observação atual.

Evidências físicas são pistas percebidas: telefone, teclado, áudio e voz
do contato, conforme a etapa. Não são sistemas internos nem documentos
que a pesquisa tenha coletado. O áudio exato de abertura/espera e eventual
protocolo emitido são L. O som de uma mensagem pode ser barreira para um
usuário, em vez de evidência acessível suficiente para todos.

## 3. Etapas e regras de ramificação do AS-IS

O cadastro de etapas abaixo fixa a linguagem usada na entrevista, matriz
e diagrama. As etapas são ações ou experiências do cidadão, não nomes de
departamentos.

| ID | Etapa | Fonte e condição |
| --- | --- | --- |
| E1 | Busca informação e liga | Início pela necessidade do cidadão; chamada em R2 p.3/13; barreira prévia é risco I |
| E2 | Ouve menu e escolhe opção | Navegação DTMF descrita em R2 p.13/15 |
| E3 | Informa identificação solicitada | CPF fornecido no caso; validação técnica e base exata L |
| E4 | Recebe resposta automática | Informação padronizada descrita em R2 p.13 |
| E5 | Solicita pessoa e aguarda | Ramo de busca por atendimento humano, quando procurado; R2 p.13 |
| E6 | Explica demanda ao atendente | Interação humana e consultas sequenciais descritas em R2 p.13–14 |
| E7 | Recebe orientação ou encaminhamento | Resposta conclusiva ou inconclusiva no relato, R2 p.13–15 |
| E8 | Encerra, procura destino ou volta a ligar | Possibilidades de saída e recontato; não constituem um procedimento único obrigatório |

**Regra de D1:** E1–E4 compõem o caminho automatizado descrito. Após E4,
o contato pode terminar; isso não prova que a dúvida foi resolvida. Se o
cidadão busca atendimento humano, segue para E5/E6, quando consegue
acessá-lo. E7 pode trazer orientação suficiente ou indicar outro órgão.
Em E8, procurar outro canal é uma nova interação; voltar a ligar reinicia
a tentativa em E1. Interrupção pode ocorrer antes e durante a espera.
Essas são alternativas do diagnóstico, não uma máquina de estados
implantada ou uma medição de frequência de cada ramo.

Não há prova de transferência automática para MTE/SINE, compartilhamento
de histórico, retorno pactuado, login gov.br, biometria ou APIs unificadas
na URA analisada. Tais elementos não entram no AS-IS. A referência ao
contato no 0800 é corroborada pela FAQ CAIXA [R4]; concessão e questões
do domínio do benefício continuam com o MTE [R3].

## 4. Quem atua e em qual camada

| Ator com nome estável | Papel na operação ou dependência | Camada e limite |
| --- | --- | --- |
| Cidadão | Inicia, escolhe, informa dado, espera e recebe a orientação | Ações do cidadão; diversidade de acesso não observada diretamente |
| URA CAIXA | Menu e resposta automatizada descritos no caso | Frontstage; mecanismos internos da URA não são o áudio percebido |
| Atendente N1 | Conversa com cidadão e consulta informações | Fala no frontstage; consulta/interpretação no backstage, conforme a ação |
| Analista CAIXA N2 | Tratamento de exceções conforme papel descrito no caso | Retaguarda condicional; contato direto em chamada específica não verificado |
| Gestor do serviço CAIXA | Função de organização do canal e capacidade | Suporte organizacional I; unidade e procedimento vigentes L |
| Suporte técnico da URA | Função de sustentação do canal | Suporte técnico I; prestador e plataforma L |
| MTE | Domínio administrativo do benefício | Dependência externa; não é atendente ao vivo em toda ligação |
| Dataprev | Ecossistema de informação e tecnologia citado no caso | Suporte/informação externa; não há prova de consulta direta URA–CNIS |
| Rede SINE/SRTE | Destino complementar conforme competência e acesso | Outra interação se o cidadão a buscar; não transferência integrada |

Na **Linha de Interação**, o Cidadão cruza a interface com URA ou N1.
Na **Linha de Visibilidade**, o que é ouvido/vivenciado fica acima e
consulta/interpretação interna fica abaixo. N1 pode cruzá-la sem que haja
troca de profissional. A **Linha de Interação Interna** separa atividades
de bastidor dos processos que as sustentam, como telefonia, fila, acesso
a sistemas e recursos organizacionais. Uma base não é uma ação humana;
ela é suporte de uma consulta.

Os sistemas SISDE/SIISO e informações de MTE/Dataprev são citados em R2
p.13 no contexto do atendimento humano. Sua presença na fonte não permite
desenhar que a URA consulta automaticamente todos eles. O modo de acesso,
as telas e os passos de registro continuam L. Não há gravações, CPFs,
credenciais ou registros pessoais nesta entrega.

## 5. Sete fail points e seus efeitos

| ID | Etapa | Gatilho e evidência | Efeito no AS-IS e desconhecido |
| --- | --- | --- | --- |
| F01 | E1/E2 | Barreira de áudio, interação ou compreensão do menu: C em R2 p.15; impedimento prévio I | Erro, necessidade de ajuda ou interrupção possível; população excluída não medida |
| F02 | E3 | Identificador não localizado: C em R2 p.14 | Dificuldade de prosseguir e orientação genérica; não sabemos regra ou base de validação |
| F03 | E4 | Informação automática genérica: C em R2 p.13 | Dúvida pode persistir e motivar busca humana; não há medida de compreensão nesta pesquisa |
| F04 | E5 | Espera com incerteza: C em R2 p.13 | Permanecer ou interromper; abandono é possibilidade I sem taxa observada nem limiar de vinte minutos |
| F05 | E6 | Indisponibilidade de informação/sistema: C em R2 p.14 | Consulta fica limitada e pode haver orientação de retorno; causa técnica específica L |
| F06 | E6 | Divergência entre dados: C em R2 p.14 | Há informação incompatível, mas N1 pode não ter competência para corrigir; destino exato depende do caso |
| F07 | E7/E8 | Encaminhamento inconclusivo/circular: C em R2 p.14–15 | Cidadão procura outro canal ou recontata; não há garantia de resolução ou recuperação integrada do histórico |

**Regra de D2:** em F05 não há informação disponível para interpretar;
em F06 pode haver informação que não coincide. O blueprint e o diagrama
devem conservar essa diferença e impedir que uma consulta falha produza
automaticamente uma resposta conclusiva. Não se atribui toda divergência
ao suporte técnico nem se concede ao atendente poder de corrigir dados
externos. **Regra de D3:** F01 não é resolvido pela suposição de um canal
acessível integrado; a barreira permanece no diagnóstico.

## 6. Normas, temporalidade e lacunas verificáveis

R6 é referência do programa; R7 trata de dados pessoais; R8 de direitos
do usuário e atendimento. As fontes delimitam perguntas de investigação,
sem atestar conformidade do canal nem resolver elegibilidade individual.
Os textos internos FP128/FP051 permanecem apenas citados no estudo.

Não se somam estimativas de fases do caso para declarar tempo de jornada
atual; média de chamada e duração completa não são a mesma unidade. A
taxa histórica de recontato não mede resolução, abandono ou causalidade
de cada falha. As lacunas a validar são arquitetura de identificação,
consulta/acesso de dados, fila, registros, atuação N2 e continuidade entre
canais. O AS-IS não fecha essas perguntas introduzindo melhorias TO-BE.

## 7. Preservação dos tratamentos da auditoria 1

A1-01 permanece atendido pela separação de ação visível, consulta e
suporte. A1-02 está mantido em E2/E3 e no limite entre identificação e
autenticação. A1-03 está aprofundado no catálogo F01–F07 com fonte e efeito.
A1-04 está atendido no enquadramento normativo e na limitação das fontes
internas. D1–D3 foram acionados explicitamente por A2-01–A2-03, e
servirão de decisões a confirmar na autoentrevista técnica.

## Fontes

- **R1:** aula04.pdf fornecida pelo aluno, 51 páginas, criada em 12/11/2026; páginas PDF 24–40. SHA-256 `b6c0572adc13e0ad6c01473246ae0bd9136bfdf382c72cc40a4efe1c48510007`. O PDF público de mesmo nome é outro arquivo.
- **R2:** [Estudo de caso da URA](https://github.com/alexlopespereira/idp_governodigital/blob/main/trabalho_final/seguro-desemprego-ura-caixa.pdf), páginas PDF 5–6 e 12–15; diagnóstico com dados de 2025.
- **R3:** [Serviço do MTE](https://www.gov.br/pt-br/servicos/solicitar-o-seguro-desemprego), etapas e competências; consulta em 14/11/2026.
- **R4:** [FAQ CAIXA](https://www.caixa.gov.br/beneficios-trabalhador/seguro-desemprego/perguntas-frequentes/Paginas/default.aspx), canal e competência; conteúdo institucional indexado em 14/11/2026.
- **R5:** [Mapa de atores do 2.1](https://github.com/contatomaycon/transformacao-digital/blob/main/exercicios/2.1/C_mapa_atores.md), apoio para identificar papéis; recomendações não importadas como operação existente.
- **R6:** [Lei 7.998/1990](https://www2.camara.leg.br/legin/fed/lei/1990/lei-7998-11-janeiro-1990-366029-normaatualizada-pl.html), referência do programa.
- **R7:** [Lei 13.709/2018](https://www2.camara.leg.br/legin/fed/lei/2018/lei-13709-14-agosto-2018-787077-normaatualizada-pl.html), dados pessoais.
- **R8:** [Lei 13.460/2017](https://legis.senado.leg.br/norma/17711251/publicacao/17711260), direitos do usuário e atendimento.
