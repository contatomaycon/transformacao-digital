# Service Blueprint AS-IS — atendimento ao Seguro-Desemprego pela URA CAIXA

**Aluno:** Maycon Douglas — TD-2026-03. **Data:** 14/11/2026.
**Serviço/canal:** Atendimento ao Seguro-Desemprego pela Unidade de Resposta
Audível da Caixa Econômica Federal, CAIXA Cidadão 0800 726 0207.
**Produção:** agente Codex, por delegação do aluno.

## 1. Recorte e regra de leitura

Este blueprint retrata o **AS-IS documental descrito no estudo de caso**,
com dados de 2025, pesquisado em 14/11/2026. Não houve ligação de teste,
observação dos sistemas ou entrevista com operadores. A aula04.pdf
fornecida pelo aluno orienta as cinco camadas e três linhas. As
recomendações de melhoria do 2.1 não foram importadas como operação atual.
Esse recorte foi decidido na [rodada 1, G01](C_grill_transcript.md).

**C:** descrição no estudo, com página; **F:** fonte institucional ou
normativa; **I:** inferência funcional, sem implementação comprovada;
**L:** detalhe não levantado. Não se preenche uma lacuna com uma solução
TO-BE. As oito etapas são as da rodada 2, G02; a sequência é condicional.

## 2. Matriz de oito etapas e cinco camadas

As colunas começam na necessidade do cidadão, antes do atendimento humano.
As três linhas divisórias valem em toda a largura. Espaços vazios nessas
linhas indicam fronteira, não uma atividade ou um dado ausente.

| Camada / etapa | E1 — Busca informação e liga | E2 — Ouve menu e escolhe opção | E3 — Informa identificação solicitada | E4 — Recebe resposta automática | E5 — Solicita pessoa e aguarda | E6 — Explica demanda ao atendente | E7 — Recebe orientação ou encaminhamento | E8 — Encerra, procura destino ou volta a ligar |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **Evidências Físicas** | Telefone e tentativa de ligação; áudio inicial L | Opções faladas e teclado [C] | Solicitação ouvida e dado digitado no telefone [C] | Mensagem padronizada ouvida [C] | Espera percebida; áudio de fila não transcrito [L] | Voz do Atendente N1 e informação comunicada [C] | Orientação verbal ou indicação de canal [C] | Fim de contato ou nova tentativa; protocolo/documento não verificado [L] |
| **Ações do Cidadão** | Percebe a dúvida e disca o canal | Ouve opções e seleciona a que interpreta adequada | Fornece o identificador solicitado, conforme o caso | Ouve e tenta compreender a resposta | Busca atendimento humano e aguarda, se desejar/conseguir | Explica sua dúvida e responde ao diálogo | Recebe e interpreta o que pode fazer a seguir | Encerra; ou busca destino; ou recomeça a tentativa |
| **Linha de Interação** | | | | | | | | |
| **Frontstage — visível/perceptível** | Entrada no canal URA descrita no caso [C] | URA CAIXA apresenta menu [C] | URA solicita identificação [C] | URA comunica informação automática [C] | Tentativa de acesso ao atendimento humano [C] | N1 conversa e orienta [C] | N1 comunica resultado ou limitação [C] | Fim da ligação; outro contato somente se buscado [C] |
| **Linha de Visibilidade** | | | | | | | | |
| **Backstage — invisível ao cidadão** | Estabelecimento da sessão [I]; mecanismo L | Tratamento da opção [I]; regra L | Tratamento/localização do identificador; mecanismo e base L | Preparação da resposta [I]; regra e origem exatas L | Organização de contatos e disponibilidade de operador [I]; lógica L | N1 consulta/interpreta informações [C]; N2 como retaguarda condicional [C] | Interpretação e limite de tratamento da exceção [C] | Continuidade entre contatos L; retomada pelo cidadão descrita no caso [C] |
| **Linha de Interação Interna** | | | | | | | | |
| **Processos de Suporte** | Telefonia e sistema de atendimento [I]; Suporte técnico da URA como função [I] | Configuração de menu e telefonia [I] | Recurso de cadastro/identificação: implementação L | Conteúdo configurado [I]; fonte técnica específica L | Fila/capacidade [I]; funções de gestão e suporte [I], fornecedor/SLA L | SISDE/SIISO e informações MTE/Dataprev citados no estudo [C]; interfaces/acessos vigentes L | Competências do MTE [F] e fontes da orientação; sem integração presumida | Canais de destino independentes; recuperação integrada de histórico não verificada [L] |
| **⚠ Fail points** | F01: barreira de acesso possível | F01: menu/acesso/compreensão | F02: identificador não localizado | F03: resposta genérica | F04: espera/incerteza e possível interrupção | F05: informação indisponível; F06: dados divergentes | F07: encaminhamento inconclusivo | F07: busca de outro canal/recontato possível; fim não prova resolução |

## 3. O significado das linhas e a passagem do mesmo profissional

Conforme as **rodadas 4–6, G04–G06**, a Linha de Interação separa o que o
Cidadão faz do contato com o serviço. A Linha de Visibilidade distingue
o que ele percebe das consultas e interpretações ocultas. A Linha de
Interação Interna separa esse trabalho dos recursos/processos de suporte.

O **Atendente N1 falando** está no frontstage de E6/E7; o **Atendente N1
consultando** está no backstage de E6. É o mesmo papel cruzando a
visibilidade, não uma equipe nova. A consulta não é a base: SISDE/SIISO
e informações de MTE/Dataprev são referências de suporte citadas no caso.
Também se distingue a URA que fala do mecanismo interno que trata uma
opção. O fato de informar CPF em E3 não comprova autenticação forte,
biometria ou consulta direta da URA ao CNIS.

## 4. Atores e dependências conservados do transcript

| Ator | Presença na matriz ou dependência | Limite da afirmação |
| --- | --- | --- |
| Cidadão | Linha de ações, E1–E8 | Público diverso; compreensão e população excluída não medidas |
| URA CAIXA | Frontstage automatizado, E1–E5 | Menu descrito no caso, sem comprovação de IA generativa |
| Atendente N1 | Frontstage E6/E7 e backstage E6 | Ação visível e consulta interna são distintas |
| Analista CAIXA N2 | Retaguarda condicional em E6 | Papel descrito no estudo; participação em chamada concreta L |
| Gestor do serviço CAIXA | Função de organização/capacidade de suporte | Unidade e procedimento operacional L, função I |
| Suporte técnico da URA | Sustentação do canal e seus recursos | Prestador, plataforma e fluxo de incidente L, função I |
| MTE | Competência do benefício e informação externa, E6–E8 | Não é agente ao vivo em cada ligação nem API presumida |
| Dataprev | Ecossistema de informação citado para E6 | Não implica conexão URA–CNIS ou poder de N1 para alterar dados |
| Rede SINE/SRTE | Destino possível em nova interação de E8 | Acesso/encaminhamento segundo competência, sem transferência automática |

Todos esses nomes aparecem na **rodada 3, G03**. Telefonia, fila,
conteúdo e SISDE/SIISO foram tratados na **rodada 6, G06**. Não se
adicionou ator ou sistema sem base na pesquisa e no transcript.

## 5. Sete fail points: evento, efeito e limite

| ID | Etapa | Evento e localização na fonte | Efeito que pode ser percebido | Limite de diagnóstico |
| --- | --- | --- | --- | --- |
| F01 | E1/E2 | Barreiras de áudio, interação e compreensão; estudo p.15 [C]; impedimento anterior à navegação [I] | Dificuldade de acesso, erro de escolha ou necessidade de ajuda | Não medimos quem não chegou ao canal nem presumimos alternativa integrada |
| F02 | E3 | Identificador não localizado; estudo p.14 [C] | Impossibilidade de seguir como esperado ou orientação genérica | Regra, cadastro consultado e mecanismo de autenticação L |
| F03 | E4 | Resposta padronizada pouco acionável; estudo p.13 [C] | Dúvida persiste; cidadão pode buscar pessoa | Sem medir compreensão ou afirmar falha em toda resposta automática |
| F04 | E5 | Espera e incerteza; estudo p.13 [C] | Aguarda ou pode interromper [I] | Sem taxa de abandono nem tempo atual/limiar de vinte minutos |
| F05 | E6 | Indisponibilidade de sistema/informação; estudo p.14 [C] | Consulta limitada, orientação de retorno ou outro canal | Informação não obtida; causa técnica específica L |
| F06 | E6 | Divergência de dados; estudo p.14 [C] | Informação incompatível e limite de correção de N1 | Diferente de F05; não se atribui competência de correção externa ao atendente |
| F07 | E7/E8 | Orientação inconclusiva e circulação entre instituições; estudo p.14–15 [C] | Busca de destino ou repetição do contato | Não é transferência automática, resolução garantida ou proporção medida de pessoas |

O catálogo corresponde à **rodada 8, G08**. F05 e F06 têm mecanismos e
limites diferentes: não obter informação não é o mesmo que receber
informação divergente. A barreira de F01 atravessa entrada e menu,
conforme **rodada 9, G09**. Não foi criada uma solução TO-BE para
preencher a ausência de observação.

## 6. Saídas, retorno e fronteira externa

Conforme **rodada 7, G07**, o fluxo pode sair de E4 diretamente para
E8 quando a ligação termina. Se o cidadão busca pessoa, existe o ramo
E5/E6, condicionado ao acesso humano. Após E7, a orientação pode ser
conclusiva ou inconclusiva. Em E8, procurar MTE/Rede SINE/SRTE é outra
interação; voltar a ligar retorna a E1. Interrupção pode ocorrer antes
ou durante a espera. Esses resultados são categorias analíticas, não
estados comprovados de um CRM.

Terminar a ligação não comprova resolver a dúvida. O diagnóstico não
inclui protocolo unificado, callback, compartilhamento de histórico,
acompanhamento pactuado, login gov.br ou API de integração como operação
existente. Não se transforma concessão ou recurso em atividade do menu.

## 7. Decisões e rastreabilidade

| Escolha no blueprint | Rodada/decisão | Onde foi aplicada |
| --- | --- | --- |
| AS-IS documental do caso, sem teste ao vivo | 1/G01 | Recorte e grau de evidência |
| Oito ações na ótica do cidadão | 2/G02 | Colunas E1–E8 |
| Cinco faixas e três linhas explícitas | 4/G04 | Matriz e interpretação das fronteiras |
| N1 cruza a visibilidade conforme a ação | 5/G05 | Frontstage e backstage em E6 |
| Identificação e base de suporte não presumidas | 6/G06 | E3/E6 e limites técnicos |
| Saídas e recontato condicionais | 7/G07 | Alternativas de E4/E8 e E8/E1 |
| Sete falhas rastreadas | 8/G08 | Linha de fail points e catálogo |
| Barreiras e desconhecidos preservados | 9/G09 e 12/G12 | F01, campos L e ausência de solução futura |

## 8. Fontes e limites

- **Método:** aula04.pdf fornecida pelo aluno, *Aula 04 — Desenho de Serviços Centrado no Usuário*, 51 páginas, criada em 12/11/2026; páginas PDF 24–40, especialmente 29–32,35,40. SHA-256 `b6c0572adc13e0ad6c01473246ae0bd9136bfdf382c72cc40a4efe1c48510007`. Não é o PDF público antigo de mesmo nome.
- **Operação documental:** [estudo da disciplina](https://github.com/alexlopespereira/idp_governodigital/blob/main/trabalho_final/seguro-desemprego-ura-caixa.pdf), páginas PDF 5–6 e 12–15, diagnóstico com dados de 2025.
- **Fronteiras institucionais:** [MTE](https://www.gov.br/pt-br/servicos/solicitar-o-seguro-desemprego) e [FAQ CAIXA](https://www.caixa.gov.br/beneficios-trabalhador/seguro-desemprego/perguntas-frequentes/Paginas/default.aspx), consultados em 14/11/2026; FAQ por conteúdo institucional indexado.
- **Contexto normativo:** [Lei 7.998/1990](https://www2.camara.leg.br/legin/fed/lei/1990/lei-7998-11-janeiro-1990-366029-normaatualizada-pl.html), [Lei 13.709/2018](https://www2.camara.leg.br/legin/fed/lei/2018/lei-13709-14-agosto-2018-787077-normaatualizada-pl.html) e [Lei 13.460/2017](https://legis.senado.leg.br/norma/17711251/publicacao/17711260): referências de programa, dados e atendimento, sem declaração de conformidade.

Os mecanismos de identificação, consultas, fila, registros e continuidade
exigem levantamento operacional para confirmação. Os tempos e indicadores
históricos não foram convertidos em medições atuais. O diagnóstico não
inclui dados pessoais nem gravações de cidadãos. A Parte D usa os mesmos
IDs, atores, alternativas e limitações deste blueprint.
