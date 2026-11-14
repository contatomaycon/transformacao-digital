# Autoentrevista `/grill-me` — decisões do Service Blueprint AS-IS

**Data:** 14/11/2026. **Contexto:** [pesquisa v3](B_relatorio_assistente_v3.md),
aula04.pdf fornecida e [mapa do 2.1](https://github.com/contatomaycon/transformacao-digital/blob/main/exercicios/2.1/C_mapa_atores.md).
**Entrevistador/respondente:** agente Codex, executando as decisões
delegadas pelo aluno. Registro integral da autoentrevista técnica, com uma
pergunta por rodada. As decisões G01–G12 orientam a matriz e o diagrama.

## Rodada 1 — Que AS-IS podemos afirmar?

**Pergunta:** Devemos apresentar o fluxo como observação da URA hoje ou
como diagnóstico documental? Recomendo delimitar o período e preservar o
serviço do 2.1, sem importar suas propostas como fatos.

**Resposta:** Escolho o **Atendimento ao Seguro-Desemprego pela URA CAIXA**,
CAIXA Cidadão 0800 726 0207. O AS-IS será o descrito no estudo com dados
de 2025, pesquisado documentalmente em 14/11/2026. Não houve ligação de
teste nem observação de bastidores. Fontes oficiais atuais delimitam
competências, não comprovam todos os passos internos. O objeto começa
na necessidade de informação e termina no contato, no encaminhamento ou
na tentativa seguinte; não inclui conceder o benefício. **G01:** recorte
informacional e temporalidade explícitos em C e D.

## Rodada 2 — Quais etapas pertencem à ótica do cidadão?

**Pergunta:** Que sequência deve orientar as colunas da matriz, antes de
listar departamentos? Recomendo fixar as oito etapas da v3.

**Resposta:** Adoto exatamente: **E1 Busca informação e liga**;
**E2 Ouve menu e escolhe opção**; **E3 Informa identificação solicitada**;
**E4 Recebe resposta automática**; **E5 Solicita pessoa e aguarda**;
**E6 Explica demanda ao atendente**; **E7 Recebe orientação ou
encaminhamento**; **E8 Encerra, procura destino ou volta a ligar**.
Não são oito etapas obrigatórias de toda ligação. A experiência começa
antes do balcão ou da consulta interna. Separar E2 e E3 permite tratar a
falha de identificação sem confundi-la com escolha de menu. **G02:**
nomes e IDs estáveis nas colunas, falhas e diagrama.

## Rodada 3 — Quais atores e funções entram na operação?

**Pergunta:** Quais atores do 2.1 são necessários ao blueprint e quais
dependências não equivalem a atendentes ao vivo? Recomendo um recorte
operacional, sem inserir toda a governança em cada chamada.

**Resposta:** Os nomes estáveis serão **Cidadão**, **URA CAIXA**,
**Atendente N1**, **Analista CAIXA N2**, **Gestor do serviço CAIXA**,
**Suporte técnico da URA**, **MTE**, **Dataprev** e **Rede SINE/SRTE**.
Gestor e suporte são funções de sustentação, com unidade/prestador
desconhecidos. N2 é retaguarda condicional do caso. MTE mantém competência
administrativa e Dataprev é dependência de informação/tecnologia; não
participam necessariamente da chamada. Rede SINE/SRTE pode ser destino
de uma nova interação. **G03:** nove papéis delimitados; não transformar
o mapa amplo de atores em uma sequência obrigatória de atendimento.

## Rodada 4 — Onde ficam as cinco camadas e três linhas?

**Pergunta:** Como impedir que a matriz seja apenas uma jornada com
emoções? Recomendo explicitar todas as faixas da aula anexada.

**Resposta:** As faixas serão **Evidências Físicas**, **Ações do Cidadão**,
**Frontstage**, **Backstage** e **Processos de Suporte**. A **Linha de
Interação** fica entre ações do cidadão e contato com o serviço; a
**Linha de Visibilidade** separa o que se percebe das consultas e
interpretações ocultas; a **Linha de Interação Interna** fica entre esse
trabalho e os processos/recursos de sustentação. No telefone, áudio,
teclado e voz são pistas perceptíveis, e não só papel ou tela. Uma base
interna não é evidência física recebida pelo usuário. **G04:** oito
colunas de etapas, cinco camadas e três linhas em posições explícitas.

## Rodada 5 — O mesmo N1 pode estar nos dois lados da visibilidade?

**Pergunta:** Devemos classificar todo o Atendente N1 como frontstage e
todo o sistema como backstage? Recomendo classificar ações, não congelar
pessoas inteiras em uma faixa.

**Resposta:** A voz e a conversa de N1 com o cidadão em E6/E7 são
frontstage. A consulta e a interpretação feitas por N1 fora da percepção
do cidadão são backstage, mesmo que ele continue ao telefone. A URA
apresentando menu e resposta está no frontstage; seu tratamento interno
não é o áudio que o usuário ouve. Analista CAIXA N2 fica como retaguarda
condicional; sua fala direta em chamada específica é desconhecida. **G05:**
o diagrama poderá separar N1 falando e N1 consultando, identificando que
é o mesmo papel e não duas equipes inventadas.

## Rodada 6 — Identificação e suporte técnico podem ser preenchidos por exemplo?

**Pergunta:** O fornecimento de CPF prova autenticação forte ou consulta
direta ao CNIS pela URA? Recomendo manter os mecanismos não verificados
como lacunas, distinguindo consulta de sistema de suporte.

**Resposta:** Não prova. E3 contém identificação solicitada conforme o
caso; validação, base e regra exatas são desconhecidas. O estudo cita
**SISDE/SIISO** e informações de **MTE/Dataprev** no atendimento humano.
Essas referências não comprovam API URA–CNIS. No backstage colocarei o
tratamento/consulta, e no suporte os cadastros, telefonia, sistema de
menu e mecanismo de fila, com limites de evidência. O suporte técnico e
a gestão de capacidade são dependências funcionais, sem fornecedor,
algoritmo ou SLA confirmado. **G06:** nenhuma biometria, login gov.br,
discador preditivo ou plataforma específica será inventada como AS-IS.

## Rodada 7 — A saída após autoatendimento significa resolução?

**Pergunta:** Como representar E4/E5 e E7/E8 sem obrigar todos a procurar
pessoa e voltar a ligar? Recomendo conservar as alternativas de D1 da v3.

**Resposta:** Depois de E4, a ligação pode terminar; isso só comprova
fim de contato, não compreensão da dúvida. Se o cidadão busca pessoa,
há o ramo E5 e, quando acessível, E6. Em E7 a orientação pode ser
conclusiva ou inconclusiva. Em E8, encerrar, buscar outro canal e
recontatar são possibilidades diferentes. O retorno E8 → E1 será marcado
“se volta a ligar”. Uma indicação de MTE ou Rede SINE/SRTE é outra
interação, sem transferência automática ou histórico unificado comprovado.
**G07:** classificações de resultado, não estados implantados em um CRM
nem protocolo de seguimento TO-BE do 2.1.

## Rodada 8 — Quais falhas serão mantidas visíveis?

**Pergunta:** Quais fail points precisam aparecer por etapa, com efeitos
concretos e sem inventar medidas? Recomendo usar os sete IDs finais da v3.

**Resposta:** Registro **F01** barreira de acesso/compreensão em E1/E2;
**F02** identificador não localizado em E3; **F03** resposta genérica em
E4; **F04** espera e possível interrupção em E5; **F05** indisponibilidade
de informação/sistema em E6; **F06** divergência de dados em E6; **F07**
encaminhamento inconclusivo/circular em E7/E8. Em F05 a informação não
foi obtida; em F06 pode haver informação incompatível que N1 não pode
corrigir. Não usarei fila superior a vinte minutos, frequência de falha
ou causa de infraestrutura sem evidência. **G08:** IDs e efeitos iguais
na matriz, catálogo e diagrama, mantendo separado o que não se sabe.

## Rodada 9 — Quem nem consegue chegar ao menu desaparece do mapa?

**Pergunta:** Como representar acessibilidade sem criar uma solução
futura que pareça existente? Recomendo tratar a barreira como transversal,
com grau de evidência explícito.

**Resposta:** F01 alcança E1/E2. O estudo descreve dificuldades com áudio,
DTMF e linguagem; a possibilidade de impedimento antes da navegação é
inferência, não população medida. Telefone, som e teclado não significam
acesso autônomo para qualquer pessoa. Não acrescentarei intérprete,
videochamada, aplicativo integrado ou atendimento acessível hipotético
como nova etapa do AS-IS. No limite da evidência física, o áudio exato
da abertura/espera não foi transcrito nem a compreensão foi testada.
**G09:** explicitar a lacuna e a barreira, preservando o diagnóstico sem
preenchê-lo com desenho TO-BE.

## Rodada 10 — O que as normas permitem afirmar?

**Pergunta:** Podemos transformar a lista de leis em prova de conformidade
ou regras de acesso aos sistemas? Recomendo usá-las para delimitar o
contexto e as perguntas de investigação.

**Resposta:** A Lei 7.998/1990 referencia o programa, a Lei 13.709/2018
trata de dados e a Lei 13.460/2017 de direitos do usuário. Não declaro
conformidade, elegibilidade ou procedimento de autenticação a partir
desses títulos. FP128/FP051 só foram citadas pelo estudo, sem leitura
interna. O trabalho não terá CPF, gravação, credencial ou caso pessoal.
O PDF fornecido é a fonte do método, com páginas e hash identificados,
sem atribuí-lo ao arquivo público antigo de mesmo nome. **G10:** manter
referências e limites, sem inferir autorização de consulta ou comprovação
de operação atual.

## Rodada 11 — Como o diagrama deriva da matriz?

**Pergunta:** Que ligações precisam aparecer para que D seja mais que
uma lista de caixas? Recomendo a sequência condicional E1–E8 e vínculos
explícitos com interface, bastidor e suporte.

**Resposta:** Mostrarei setas entre etapas, a saída E4 → E8, o ramo
humano E4 → E5 → E6 → E7 e o retorno condicional E8 → E1. Os vínculos
com URA CAIXA e N1 falando indicam contato; N1 consultando e N2 indicam
bastidor; telefonia, fila e SISDE/SIISO são suporte, com evidência
qualificada. MTE/Dataprev serão dependências de competência/informação,
não chamadas de API comprovadas. A Rede SINE/SRTE só aparece como
destino externo se buscado. F05/F06 não podem virar consulta bem-sucedida
automaticamente no desenho. **G11:** relações rotuladas, legenda de
evidência e tabela de correspondência com C.

## Rodada 12 — O que fica decidido e o que continua desconhecido?

**Pergunta:** Há etapa ou ator que surgirá na matriz sem ter sido
discutido? Recomendo conferir nomes e preservar desconhecidos reais.

**Resposta:** Todos os oito nomes de etapas foram fixados na rodada 2,
os nove atores na rodada 3, os recursos e as camadas nas rodadas 4–6 e
as sete falhas na rodada 8. Estão decididos recorte, linhas, classificação
de ações, alternativas e relações. Permanecem desconhecidos arquitetura
de identificação, interfaces de consulta, plataforma de fila, registros,
papel N2 em chamada específica e continuidade de histórico entre canais.
As estimativas de tempo e o recontato do estudo não serão convertidos em
medidas atuais de jornada ou resolução. **G12:** o diagnóstico encerra
com limites explícitos; não haverá ação ou tecnologia adicional em C/D
sem suporte neste registro e na pesquisa.

## Índice das decisões

G01 recorte/tempo; G02 etapas; G03 atores; G04 camadas/linhas; G05 ações
visíveis/ocultas; G06 identificação/suporte; G07 saídas e loops; G08 falhas;
G09 barreiras; G10 fontes/normas; G11 diagrama; G12 limites finais.
Este é um exercício documental com autoentrevista técnica, não relato de
entrevista de campo com servidores ou de ligação realizada à CAIXA.
