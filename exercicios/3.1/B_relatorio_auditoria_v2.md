# Auditoria 2 — saídas condicionais, falhas diferentes e barreiras de entrada

**Objeto:** `B_relatorio_assistente_v2.md`. **Revisor:** agente Codex,
segunda revisão crítica, 14/11/2026. O exame verifica os tratamentos
anteriores e procura lacunas remanescentes relevantes para o AS-IS.

## 1. Conferência da auditoria anterior

| Achado | O que a v2 fez | Situação |
| --- | --- | --- |
| A1-01 | Separou cinco dimensões por etapa e distinguiu N1 falando de N1 consultando | Resolvido como estrutura da pesquisa; preservar na matriz final |
| A1-02 | Criou E2/E3 separadas e marcou mecanismo de identificação como L | Resolvido; não converter CPF em autenticação forte na Parte C |
| A1-03 | Criou F01–F06 com etapas e efeitos, sem inventar frequência ou SLA | Resolvido em nível geral; F05 ainda reúne exceções diferentes, conforme A2-02 |
| A1-04 | Incluiu fontes oficiais do programa, dados e usuário e limitou normas internas | Resolvido no enquadramento; não equivale a auditoria de conformidade |

## A2-01 — As alternativas de saída ainda cabem em uma única coluna

**Trecho:** “E8 — Encerra, procura destino ou volta a ligar”. A v2 avisa
que a jornada é condicional, porém não define como essa condição será
transportada à matriz e ao diagrama. Há risco de desenhar E1 → E8 como
caminho obrigatório, exigindo atendimento humano e recontato em toda
chamada, ou de confundir fim de ligação com dúvida resolvida.

O estudo, páginas PDF 13–14, distingue resposta conclusiva e resposta
inconclusiva, além da recorrência. A v3 precisa explicitar a saída após
resposta automática, o ramo humano quando buscado e os resultados após
orientação. Deve mostrar retorno à tentativa de contato como possibilidade,
não como porcentagem de pessoas ou desfecho obrigatório. São classificações
analíticas de resultados, não estados implantados em um CRM ou protocolo
compartilhado. **Aceite:** regras textuais de ramificação, sem inventar
um acompanhamento integrado que só foi proposto no 2.1.

## A2-02 — Indisponibilidade e divergência não são o mesmo fail point

**Trecho:** F05 reúne “Sistema indisponível ou dados divergentes”. Nos
dois casos o usuário pode receber orientação insuficiente, mas o trabalho
de bastidor é diferente. Na indisponibilidade, não se obtém a informação;
na divergência, o problema é a incompatibilidade entre informações ou
cadastros. Agrupar as ocorrências pode levar a atribuir ambas a suporte
técnico ou a inventar que o atendente pode corrigir um dado externo.

R2, página PDF 14, descreve as ocorrências separadamente. A v3 deve
desdobrá-las, explicitar o efeito percebido e manter desconhecida a
causa de infraestrutura ou o canal exato de correção quando a fonte não
o documenta. Um diagrama de consulta com resultado indisponível não pode
mostrar o mesmo dado como consultado com sucesso na etapa seguinte.
**Aceite:** identificadores diferentes, ramo de falha coerente e limite
de competência preservado.

## A2-03 — A barreira de acesso pode ocorrer antes de navegar no menu

**Trechos:** F01 foi ligado apenas a E2 e E1 apresenta “entrada na URA”.
O levantamento ainda pode invisibilizar quem não chega a ouvir ou
compreender o canal, apesar de a aula exigir perspectiva de quem consome
e de o estudo descrever barreiras auditivas e de interação.

A aula anexada, páginas PDF 31, 35 e 40, destaca a interface acessível e
as pistas percebidas. A v3 deve admitir que a barreira pode atingir E1/E2,
sem afirmar que mediu pessoas excluídas ou que existe alternativa integrada
já resolvida. Convém distinguir a descrição do estudo sobre o menu da
inferência sobre impedimento anterior à chamada. Também é necessário
lembrar que uma evidência física no telefone pode ser perceptível por
áudio/teclado, e não necessariamente um documento de papel.
**Aceite:** limite de evidência e fail point transversal explícitos, sem
criar uma etapa TO-BE de acessibilidade para preencher a lacuna.

## 2. Condições para a versão final

A v3 deve indicar um delta para cada gatilho A2-01 a A2-03, manter a
separação das cinco camadas e preservar os quatro tratamentos de A1.
As mudanças precisam alterar o raciocínio operacional, não só títulos:
saídas e loops coerentes; consulta sem informação separada de informação
divergente; e possibilidade de exclusão antes da navegação. Não é
necessário inventar mecanismo técnico, autenticação ou entrevista de campo
para preencher um desconhecido que foi corretamente identificado.
