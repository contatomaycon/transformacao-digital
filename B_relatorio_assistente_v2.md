# Revisão v2 — desagregar a jornada e qualificar o que se sabe

A primeira auditoria mostrou que agrupar interface, consulta e mecanismo
técnico obscurecia justamente o objeto do blueprint. Esta revisão separa
oito etapas e suas dependências, sem preencher as lacunas com arquitetura
presumida. O serviço continua sendo o atendimento informacional do
Seguro-Desemprego pela URA CAIXA, 0800 726 0207.

**Autoria:** agente Codex. **Pesquisa documental:** 14/11/2026.
**AS-IS de referência:** operação descrita no estudo com dados de 2025;
não é observação direta do canal em novembro de 2026.

## 1. Tratamento da auditoria 1

| Achado | Tratamento | Mudança e limite preservado |
| --- | --- | --- |
| A1-01: interface e bastidor agregados | Corrigido | As ações visíveis e ocultas são separadas por etapa. N1 pode atuar nos dois lados da visibilidade; sistemas são suporte da consulta. |
| A1-02: navegação e identificação comprimidas | Corrigido; mecanismo interno em aberto | E2 e E3 são diferentes. Informar CPF não comprova autenticação forte nem consulta direta pela URA ao CNIS. |
| A1-03: falhas sem rastreio | Corrigido | F01–F06 são ligados a etapas e efeitos. Frequência, duração e algoritmo não comprovados permanecem desconhecidos. |
| A1-04: referências normativas incompletas | Corrigido no enquadramento | Foram identificadas fontes oficiais sobre programa, dados e direitos do usuário. Não há declaração de conformidade nem acesso a normas internas. |

## 2. Legenda de evidência

**C:** descrição do estudo de caso, com período e página; **F:** informação
institucional ou normativa confirmada na fonte pública; **I:** inferência
funcional necessária para interpretar a operação, sem implementação
comprovada; **L:** detalhe não levantado. A classificação é da afirmação,
não uma certificação de todo o canal.

R1 é a aula fornecida, páginas PDF 29–32, 35 e 40. R2 é o estudo, páginas
PDF 5–6 e 12–15. R3/R4 são MTE e FAQ CAIXA, que delimitam competências.
O suporte técnico e a gestão de capacidade são funções de sustentação;
unidade, prestador e plataforma exatos continuam L.

## 3. Oito etapas na ótica do cidadão

| Etapa e ação do cidadão | Evidência física/perceptível | Frontstage | Backstage | Suporte e limite |
| --- | --- | --- | --- | --- |
| E1 — Busca informação e liga | Telefone e início de ligação; áudio inicial não transcrito | Entrada na URA CAIXA, descrita no caso | Estabelecimento e encaminhamento da sessão, mecanismo L | Telefonia e sistema de atendimento: dependência I |
| E2 — Ouve menu e escolhe opção | Opções faladas e teclado do telefone | URA apresenta menu DTMF [C] | Tratamento da opção escolhida: I; regra e plataforma L | Configuração de menu e telefonia: I |
| E3 — Informa identificação solicitada | Solicitação ouvida e dado digitado, conforme o caso | URA solicita CPF [C] | Tratamento/localização do identificador; arquitetura L | Cadastro consultado e regra exata L; não se presume CNIS direto |
| E4 — Recebe resposta automática | Mensagem padronizada sobre a consulta [C] | URA comunica informação [C] | Preparação da informação: I; sua origem técnica exata L | Conteúdo e informação disponíveis ao canal, sem API presumida |
| E5 — Solicita pessoa e aguarda | Espera percebida; áudio de fila não transcrito | Tentativa de transferência humana descrita no caso [C] | Organização do atendimento e disponibilidade de operador: I | Mecanismo de fila e capacidade: I; fornecedor e SLA L |
| E6 — Explica demanda ao atendente | Voz do Atendente N1 e conteúdo comunicado [C] | N1 conversa e orienta | N1 consulta; Analista CAIXA N2 trata exceção conforme papel descrito [C] | SISDE/SIISO e informações MTE/Dataprev citados em R2; interface e acesso vigente L |
| E7 — Recebe orientação ou encaminhamento | Resposta verbal ou indicação de outro canal [C] | N1 comunica resultado dentro de sua competência | Interpretação e limite de tratamento de exceção [C] | Regras e dependências de MTE, Dataprev e rede competente; sem protocolo compartilhado comprovado |
| E8 — Encerra, procura destino ou volta a ligar | Fim do contato ou novo contato | Ação visível de novo canal somente se buscado | Continuidade entre contatos não comprovada | Canais institucionais separados; recuperação de histórico integrada não verificada |

## 4. Camadas e limites de competência

A **Linha de Interação** separa ação do Cidadão e contato com a URA ou
Atendente N1. A **Linha de Visibilidade** separa o áudio/diálogo percebido
das consultas e interpretações internas. A **Linha de Interação Interna**
separa esse trabalho de bastidor dos processos e recursos de suporte.
As evidências físicas são as pistas percebidas, não a infraestrutura
interna que o usuário não vê.

N1 falando é frontstage; N1 consultando informação é backstage. Analista
CAIXA N2 aparece como retaguarda condicional, não como uma pessoa que
necessariamente fala em toda chamada. MTE e Dataprev não são agentes de
atendimento ao vivo na URA: o primeiro mantém competência administrativa,
e o segundo participa do ecossistema de informação/tecnologia. Rede
SINE/SRTE é possível destino de outra interação, segundo competência,
sem transferência automática comprovada.

## 5. Catálogo de falhas documentais

| ID | Etapa | Evento ou barreira | Efeito e limite |
| --- | --- | --- | --- |
| F01 | E2 | Menu difícil de compreender ou acessar [C, R2 p.15] | Escolha errada, reinício ou necessidade de ajuda; frequência L |
| F02 | E3 | Identificador não localizado [C, R2 p.14] | Atendimento não prossegue como esperado; base e regra exatas L |
| F03 | E4 | Resposta genérica sem explicação utilizável [C, R2 p.13] | Usuário tenta obter atendimento humano; compreensão não medida |
| F04 | E5 | Espera e incerteza [C, R2 p.13] | Risco de desistência I; não foi medido abandono nesta pesquisa |
| F05 | E6 | Sistema indisponível ou dados divergentes [C, R2 p.14] | Consulta limitada, orientação de retorno ou outro canal; não se nomeia causa de infraestrutura |
| F06 | E7/E8 | Encaminhamento sem solução clara [C, R2 p.14–15] | Busca de outro órgão ou recontato; a mesma ligação não é automaticamente transferida |

Os tempos apresentados no estudo são estimativas/contexto daquele
levantamento. Não estabelecemos tempo atual de fila, prazo de resposta
ou percentual de pessoas sem solução. O indicador histórico de recontato
não demonstra que toda nova chamada corresponde à mesma dúvida.

## 6. Referências normativas e desconhecidos

A Lei 7.998/1990 é referência do programa; a Lei 13.709/2018 trata de
dados pessoais; a Lei 13.460/2017 estabelece direitos do usuário e
diretrizes de atendimento. Aqui elas ajudam a formular perguntas sobre
competência, acesso, informação e barreiras. Não permitem declarar o
canal conforme ou não conforme sem examinar a operação e os procedimentos.
FP128/FP051 permanecem citações secundárias de R2, sem leitura dos textos.

Continuam em aberto: estrutura de identificação, plataforma de fila,
acessos e consultas reais, organização N1/N2, tipo de registro e
continuidade entre canais. Fechar essas lacunas exigiria documentação
operacional, observação e entrevistas autorizadas, não inferência a
partir de um fluxograma de exemplo. A revisão não incorpora login gov.br,
biometria, protocolo unificado ou acompanhamento pactuado como AS-IS.

## Referências verificáveis

- **R1:** aula04.pdf fornecida pelo aluno, 51 páginas, criada em 12/11/2026; páginas PDF 24–40. SHA-256 `b6c0572adc13e0ad6c01473246ae0bd9136bfdf382c72cc40a4efe1c48510007`.
- **R2:** [Estudo de caso da URA](https://github.com/alexlopespereira/idp_governodigital/blob/main/trabalho_final/seguro-desemprego-ura-caixa.pdf), páginas PDF 5–6 e 12–15.
- **R3:** [Serviço do MTE](https://www.gov.br/pt-br/servicos/solicitar-o-seguro-desemprego), responsável e etapas; consulta em 14/11/2026.
- **R4:** [FAQ CAIXA](https://www.caixa.gov.br/beneficios-trabalhador/seguro-desemprego/perguntas-frequentes/Paginas/default.aspx), consulta e concessão; conteúdo institucional indexado em 14/11/2026.
- **R5:** [Mapa do exercício 2.1](https://github.com/contatomaycon/transformacao-digital/blob/main/exercicios/2.1/C_mapa_atores.md); fonte de papéis, não prova das melhorias propostas.
- **R6:** [Lei 7.998/1990 — Câmara](https://www2.camara.leg.br/legin/fed/lei/1990/lei-7998-11-janeiro-1990-366029-normaatualizada-pl.html), arts.1–2 e enquadramento do programa.
- **R7:** [Lei 13.709/2018 — Câmara](https://www2.camara.leg.br/legin/fed/lei/2018/lei-13709-14-agosto-2018-787077-normaatualizada-pl.html), proteção de dados pessoais.
- **R8:** [Lei 13.460/2017 — Senado](https://legis.senado.leg.br/norma/17711251/publicacao/17711260), arts.1,4–5 e direitos no atendimento público.
