# Auditoria 1 — responsabilidades, evidência e usuários omitidos

**Objeto:** `B_relatorio_assistente_v1.md`, versão inicial de 13/11/2026.
**Autoria:** revisão crítica do agente Codex, em etapa separada da pesquisa.
A auditoria examina conteúdo e evidência, sem contar formatação como falha.

## A1-01 — MTE e Dataprev foram agrupados como um único ator

**Trecho auditado:** a linha da tabela intitulada **“MTE/Dataprev”** reúne
“decisões e informações necessárias à orientação”. Isso impede identificar
quem responde por uma decisão de benefício e quem fornece processamento ou
informação. É uma deficiência substantiva do inventário: uma relação de
dependência entre duas organizações desaparece quando ambas viram um nó.

O [MTE identifica o Seguro-Desemprego como serviço de sua responsabilidade](https://www.gov.br/pt-br/servicos/solicitar-o-seguro-desemprego).
O estudo de caso, páginas PDF 5–6, descreve separadamente MTE e Dataprev.
O relatório deve criar duas linhas, conservar a distinção entre decisão
administrativa e infraestrutura tecnológica e evitar supor que um
processador de dados possui a mesma competência do gestor do benefício.
**Aceitação:** duas identidades, papéis separados e relação explícita entre elas.

## A1-02 — A métrica de recontato tem definição insuficiente

**Trecho auditado:** “12,11% de recontato por CPF no mesmo dia”. A expressão
não informa se o denominador são chamadas, CPFs únicos ou casos. Tampouco
explica se a repetição de um identificador corresponde à mesma dúvida. Isso
prejudica a interpretação do problema que orientará o mapa.

O [estudo de caso](https://github.com/alexlopespereira/idp_governodigital/blob/main/trabalho_final/seguro-desemprego-ura-caixa.pdf),
páginas PDF 2–4 e 7–9, associa o indicador a chamadas adicionais no período.
A v1 o atribui corretamente ao estudo, mas a base operacional original não
foi disponibilizada nesta coleta para recalcular a regra. A leitura de
recontato como indício é defensável; inferir causa, identidade da demanda
ou proporção de pessoas seria exceder a evidência.
**Aceitação:** registrar período e unidade, delimitar o que é relato dos
autores e manter cálculo e causalidade como pendências de validação.

## A1-03 — Faltam responsáveis verificáveis pelos encaminhamentos

**Trecho auditado:** “faltam validação dos responsáveis internos” e a
dependência do Gestor do serviço CAIXA de “conhecimento dos problemas
recorrentes”. O relatório reconhece a lacuna, porém não define qual pergunta
de validação fecha o problema. Isso permitiria que o mapa atribuísse
aprovações a uma unidade inventada ou confundisse manutenção técnica com
autoridade sobre a concessão.

A descrição de N1/N2 no estudo é evidência acadêmica contextual; não é um
organograma operacional vigente. A v2 precisa marcar as atribuições de
Gestor do serviço CAIXA e Suporte técnico da URA como funções analíticas,
identificar a evidência disponível e propor um aceite verificável para a
transferência: destino, motivo, orientação e responsável pelo seguimento.
**Aceitação:** distinguir papel conhecido, responsabilidade proposta e
pendência de confirmação institucional, sem inventar SLA ou integração.

## A1-04 — Acessibilidade e governança de dados ficaram fora da rede

**Trechos auditados:** o único usuário é “Cidadão” e acessibilidade aparece
apenas como questão para a próxima etapa. A ausência é material: um menu
de voz não cobre, por si, pessoas surdas, usuários sem internet ou pessoas
que não conseguem navegar no menu. A persona da página PDF 13 do estudo
ilustra essa barreira, mas não substitui escuta de pessoas reais.

A [CAIXA descreve atendimento em Libras](https://www.caixa.gov.br/atendimento/libras/Paginas/default.aspx)
ligado ao SAC e à rede física. Isso justifica investigar um ator de
intermediação acessível, sem afirmar integração automática com a URA. A
[página institucional de privacidade](https://www.caixa.gov.br/privacidade/Paginas/default.aspx)
também identifica o papel de encarregado de dados, relevante quando a
jornada utiliza identificadores e histórico de contatos.
**Aceitação:** incluir essas funções, suas limitações e relações; registrar
alternativa sem smartphone como necessidade a validar, não como canal já
integrado. Considerar a Ouvidoria CAIXA como voz crítica e não só depósito
de reclamações, seguindo a aula 2, páginas PDF 35–36.

## Encaminhamento para a v2

Os quatro achados exigem mudança de conteúdo. A v2 deverá apresentar uma
matriz com o tratamento individual de A1-01 a A1-04: corrigido, defendido
com evidência ou em aberto com ação de verificação. Deve preservar as
incertezas que não podem ser resolvidas por pesquisa documental. A
revisão está aprovada para orientar nova pesquisa, não para certificar
contratos, fluxos internos ou resultados atuais do serviço.
