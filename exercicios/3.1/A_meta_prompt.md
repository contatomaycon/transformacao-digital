# Meta-prompt — operação do atendimento ao Seguro-Desemprego pela URA CAIXA

## Contexto e serviço focal

Elabore um prompt para um assistente de deep research pesquisar a operação
do **Atendimento ao Seguro-Desemprego pela Unidade de Resposta Audível
(URA) da Caixa Econômica Federal**, no **CAIXA Cidadão 0800 726 0207**.
O resultado sustentará um **Service Blueprint AS-IS**, retratando como o
atendimento é descrito nas fontes disponíveis, e não uma solução futura.
O exercício continua o [mapa de atores do 2.1](https://github.com/contatomaycon/transformacao-digital/blob/main/exercicios/2.1/C_mapa_atores.md), mas
suas recomendações de melhoria não podem ser convertidas em fatos atuais.

## Método e material de contexto

Use como método a aula fornecida pelo aluno, **Aula 04 — Desenho de Serviços
Centrado no Usuário**, 51 páginas, criada em 12/11/2026, especialmente as
páginas PDF 24–40. Ela diferencia evidências físicas, ações do cidadão,
frontstage, backstage e processos de suporte, separados pelas linhas de
interação, visibilidade e interação interna. O arquivo de referência tem
SHA-256 `b6c0572adc13e0ad6c01473246ae0bd9136bfdf382c72cc40a4efe1c48510007`.
Ele não deve ser confundido com o PDF público mais antigo de mesmo nome.

Considere o [estudo de caso da disciplina](https://github.com/alexlopespereira/idp_governodigital/blob/main/trabalho_final/seguro-desemprego-ura-caixa.pdf),
sobretudo as páginas PDF 5–6 e 12–15. A data da pesquisa documental é
14/11/2026, mas o diagnóstico operacional do estudo utiliza dados de 2025.
O prompt gerado deve conservar essa diferença e identificar lacunas que
exigiriam observação ou entrevista de campo.

## Perguntas e escopo da pesquisa

Peça etapas na ótica do cidadão, começando onde ele percebe a necessidade
de informação: tentativa de contato, navegação, identificação solicitada,
resposta automática, espera, contato humano e resultado ou recontato.
Para cada etapa, solicite o que é percebido ou ouvido, a ação visível do
serviço, o trabalho oculto e as dependências técnicas/organizacionais.
Exija análise de onde o mesmo atendente cruza a linha de visibilidade.

Solicite evidências físicas ou perceptíveis, inclusive telefone, teclado,
áudios e informação recebida, sem inventar gravações, protocolos ou telas.
Peça os normativos pertinentes ao programa, ao atendimento e aos dados
pessoais, com links oficiais e limites de interpretação. Inclua fail
points de navegação, identificação, espera, consulta e encaminhamento.

## Regras de evidência e formato de saída

O prompt deve exigir relatório estruturado com pelo menos 300 palavras,
fontes e páginas, sequência de etapas, cinco camadas, linhas divisórias,
gargalos e perguntas para auditoria. Identifique separadamente descrição
do estudo, confirmação institucional, inferência funcional e detalhe não
verificado. Não pressuponha CNIS consultado diretamente pela URA, API
integrada, reconhecimento por IA, biometria ou login gov.br nesse telefone.
Identificação informada pelo cidadão não comprova autenticação forte.

Oriente o assistente a aceitar duas rodadas de crítica: cada achado deverá
ser corrigido, defendido com evidência ou mantido explicitamente em aberto.
O relatório final subsidiará uma autoentrevista de decisão, uma matriz de
no mínimo cinco etapas com as cinco camadas e um diagrama de relações
coerente com o AS-IS. O objetivo é tornar o bastidor visível ao diagnóstico,
sem transferir a complexidade institucional para o cidadão.
