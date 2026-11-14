# Auditoria 1 — separar ações, mecanismos e evidências da operação

**Objeto:** pesquisa v1 do exercício 3.1. **Revisor:** agente Codex,
em etapa crítica posterior à síntese inicial, 14/11/2026.
O exame é de conteúdo: não considera diferenças de estilo como falhas.

## A1-01 — A tabela mistura interface e trabalho oculto

**Trecho:** na coluna “Interface e trabalho de atendimento”, o momento
“Explica a dúvida ao atendente” reúne a conversa e as consultas de N1.
O texto reconhece que consultas ficam invisíveis, mas a sequência não
liga cada ação visível ao trabalho interno e à dependência de suporte.
Essa lacuna impede usar a tabela como base operacional consistente para
as cinco camadas do blueprint.

A aula fornecida, páginas PDF 29–32 e 40, exige distinguir a ação que
cruza a interface e o trabalho oculto, inclusive quando executados pelo
mesmo profissional. A v2 deve separar Atendente N1 falando com o cidadão
de Atendente N1 consultando informações, e distinguir a consulta como
ação de bastidor dos sistemas que a sustentam. Não basta colocar o ator
inteiro acima ou abaixo da linha de visibilidade.
**Aceite:** sequência com ações do cidadão, evidência percebida,
frontstage, backstage e suporte rastreáveis por etapa.

## A1-02 — Navegação e identificação foram comprimidas

**Trecho:** “Navega e fornece identificação”, acompanhado de “Erro de
opção ou identificação impede seguir a demanda”. Há dois eventos de
natureza diferente: escolha de menu e fornecimento de dado solicitado.
Agrupá-los apaga o ponto onde um identificador não localizado interrompe
a tentativa, descrito na página PDF 14 do estudo de caso.

Também é preciso impedir que “identificação” seja lida como autenticação
forte ou consulta direta ao CNIS. O estudo mostra fornecimento de CPF e
casos de não localização, mas não documenta a arquitetura exata da
validação. A v2 deve separar os momentos, explicitar o limite e distinguir
o áudio da solicitação da atividade interna que trata o dado.
**Aceite:** duas etapas, falhas específicas e mecanismo não comprovado
marcado como desconhecido, sem preencher a lacuna com exemplo do tutorial.

## A1-03 — As falhas não estão ligadas a evento e consequência

**Trecho:** “Ainda falta ligar essas exceções a cada camada e ao efeito
percebido na jornada”. A própria v1 admite o ponto. Indisponibilidade,
identificador não localizado e divergência aparecem no final, enquanto
a tabela só mostra menu, espera e saída inconclusiva. Isso deixaria os
fail points mais concretos fora do diagnóstico que sustenta a Parte C.

O estudo, páginas PDF 14–15, fornece situações suficientes para mapear
gatilho, etapa atingida e efeito: consulta interrompida, orientação
genérica, busca de outro canal ou repetição de contato. A v2 deve criar
identificadores de falha e separar ocorrência descrita de risco inferido.
Não deve inventar frequência, duração superior a vinte minutos ou causa
técnica específica. **Aceite:** cada falha ligada a etapa, evidência,
consequência e limite de verificação.

## A1-04 — O enquadramento normativo ficou incompleto

**Trecho:** “O levantamento ainda precisa organizar as demais referências
aplicáveis ao atendimento e ao tratamento de dados”. Não é uma questão
cosmética: a solicitação de identificador e o acesso a informações de
benefício dependem de competências e de tratamento de dados, enquanto
acessibilidade é parte da experiência de serviço público.

A v2 deve identificar, por fonte oficial, Lei 7.998/1990, Lei 13.709/2018
e Lei 13.460/2017 como referências de programa, dados e direitos do usuário.
Isso não autoriza declarar conformidade do canal ou interpretar uma regra
de elegibilidade individual. Os normativos internos FP128/FP051 citados
no estudo devem permanecer referências secundárias sem conteúdo presumido.
**Aceite:** fonte e finalidade delimitadas, sem afirmar leitura de documento
interno ou procedimento de autenticação que não foi observado.

## Verificações que não constituem falha

A v1 preservou o período de 2025, não disse ter feito pesquisa de campo e
não apresentou as propostas de continuidade do 2.1 como operação implantada.
Esses acertos devem permanecer. A v2 deverá tratar A1-01 a A1-04 em uma
matriz explícita de correção, defesa com evidência ou pendência verificável,
e conservar os desconhecidos que a pesquisa documental não consegue fechar.
