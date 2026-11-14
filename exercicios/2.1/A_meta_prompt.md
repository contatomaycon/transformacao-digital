# Meta-prompt — pesquisa sobre atores do atendimento do Seguro-Desemprego

## Contexto e propósito

Elabore um prompt para um assistente de deep research realizar uma pesquisa
sobre o **Atendimento ao Seguro-Desemprego pela Unidade de Resposta Audível
(URA) da Caixa Econômica Federal**, no canal telefônico CAIXA Cidadão
**0800 726 0207**. O órgão responsável pelo canal analisado é a CAIXA; a
gestão e as decisões sobre o benefício envolvem o Ministério do Trabalho e
Emprego (MTE). O problema a investigar é a dificuldade de entregar uma
orientação conclusiva sem fazer o cidadão circular entre instituições.

A pesquisa subsidiará um mapa de atores, e não um projeto de chatbot. O
recorte começa na tentativa de obter informação por telefone e termina com
orientação compreendida, encaminhamento identificado ou abandono. Aprovar
o benefício, julgar recursos e efetuar o pagamento são dependências externas
da jornada de atendimento, não decisões tomadas pelo menu de voz.

## Material de partida

Considere o [estudo de caso da disciplina](https://github.com/alexlopespereira/idp_governodigital/blob/main/trabalho_final/seguro-desemprego-ura-caixa.pdf),
especialmente as páginas PDF 3–7 e 12–14, e a
[aula 2](https://github.com/alexlopespereira/idp_governodigital/blob/main/pdfs/aula02.pdf),
especialmente as páginas PDF 31–40. O primeiro documento analisa dados de
2025 e apresenta também propostas futuras; essa temporalidade precisa
permanecer visível. Use a data de referência de 13/11/2026 para a verificação
complementar de canais oficiais.

## Perguntas que o prompt deve orientar

Solicite identificação de usuários diretos, operadores humanos, sistemas,
gestores, responsáveis por dados, fornecedores e órgãos de controle. Para
cada ator, peça papel, categoria, poder, interesse, incentivo, dependência,
limite de decisão e pontos de entrada e saída. Investigue quem atende, quem
decide, quem pode corrigir uma informação e quem responde por um
encaminhamento incompleto. Inclua necessidades de acessibilidade e vozes
críticas, evitando tomar a perspectiva gerencial como a única possível.

## Critérios de evidência

O prompt gerado deve exigir fontes primárias com links e localização do
trecho relevante. Deve distinguir fato institucional verificado, descrição
do estudo acadêmico e hipótese de desenho a validar. Oriente o assistente a
registrar páginas inacessíveis e divergências entre fontes, sem inventar
contratos, fornecedores, prazos de atendimento ou APIs existentes. Números
históricos precisam de período, definição e limitações; recontato não deve
ser tratado automaticamente como causa comprovada de falha.

## Saída e possibilidade de contestação

Peça um relatório estruturado com síntese do recorte, inventário de atores,
relações, tensões, lacunas e referências. Exija pelo menos 300 palavras e
afirmações rastreáveis. Inclua no prompt uma instrução para receber auditoria
posterior: cada crítica deverá ser corrigida, defendida com evidência ou
mantida explicitamente em aberto. A pesquisa deve preservar dúvidas úteis
para a autoentrevista de decisão e para uma futura matriz RACI, sem
apresentar atribuições propostas como organograma oficial da CAIXA.
