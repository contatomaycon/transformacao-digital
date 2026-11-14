# Transformação Digital

Repositório de exercícios da disciplina de Transformação Digital.

As atividades praticam versionamento com Git, colaboração pelo GitHub,
uso do GitHub CLI (`gh`) e automação com um agente de codificação.

## Sobre

Atividades de Maycon Douglas, da turma TD-2026-03.

Este mesmo repositório reúne as atividades. O agente auxilia na
preparação dos arquivos, no clone adicional, na colaboração por pull requests
e na avaliação pelo autograder.

No Git, `git add` prepara as alterações, `git commit` registra uma versão no
histórico local e `git push` envia os commits para o repositório no GitHub.

## Atividades

| Exercício | Prática |
| --- | --- |
| 1.1 | README, dois commits e publicação no GitHub |
| 1.2 | Autenticação no `gh`, branch, pull request e merge |
| 1.3 | Consulta e clone deste repositório com auxílio do agente |
| 1.4 | Criação de `CONTRIBUINDO.md` em uma branch e integração por PR |
| 2.1 | Mapa de atores da jornada de atendimento do Seguro-Desemprego pela URA CAIXA |

## Exercício 2.1 — Mapa de atores

**Aluno:** Maycon Douglas — TD-2026-03.

**Serviço:** Atendimento ao Seguro-Desemprego pela URA da Caixa Econômica
Federal, CAIXA Cidadão 0800 726 0207.

O trabalho reúne pesquisa, duas auditorias, revisões, autoentrevista técnica
e mapa com inventário, RACI e diagrama de relações. A produção e as decisões
foram delegadas ao agente, conforme o plano de execução.

- [A_meta_prompt.md](A_meta_prompt.md) — meta-prompt da pesquisa.
- [B_relatorio_assistente_v1.md](B_relatorio_assistente_v1.md) — pesquisa inicial.
- [B_relatorio_auditoria_v1.md](B_relatorio_auditoria_v1.md) — primeira auditoria.
- [B_relatorio_assistente_v2.md](B_relatorio_assistente_v2.md) — revisão após a primeira auditoria.
- [B_relatorio_auditoria_v2.md](B_relatorio_auditoria_v2.md) — segunda auditoria.
- [B_relatorio_assistente_v3.md](B_relatorio_assistente_v3.md) — pesquisa final com deltas rastreados.
- [C_grill_transcript.md](C_grill_transcript.md) — treze rodadas de autoentrevista e decisões.
- [C_mapa_atores.md](C_mapa_atores.md) — mapa final de treze atores, relações e responsabilidades.

O marcador [`.autograde-exercise`](.autograde-exercise) identifica o exercício
2.1. Para avaliá-lo, execute `autograde validar 2.1` na raiz deste repositório.

## Colaboração pelo GitHub CLI

Uma branch separa uma alteração do histórico principal até sua integração.
Depois de editar um arquivo nessa branch, é necessário registrar o commit
e fazer push antes de abrir o pull request.

```bash
gh auth status
gh repo view contatomaycon/transformacao-digital
git switch -c docs/minha-melhoria
# Edite os arquivos e confira as alterações antes de continuar.
git add README.md
git commit -m "docs: descreve a melhoria realizada"
git push -u origin docs/minha-melhoria
gh pr create --base main --title "docs: explica a melhoria no README" --body "Descreve a mudança e como ela foi conferida."
gh pr merge --squash --delete-branch
```

O PR apresenta a mudança para revisão. O merge integra seu conteúdo à `main`;
fechar um PR sem merge não inclui a alteração no histórico principal.

As orientações para novas alterações estão em [CONTRIBUINDO.md](CONTRIBUINDO.md).

## Avaliação

Após o setup e o login com a conta cadastrada na turma, execute o autograder
dentro deste repositório, sempre informando o ID do exercício:

```bash
autograde doctor
autograde validar 1.1
autograde validar 1.2
autograde validar 1.3
autograde validar 1.4
autograde validar 2.1
autograde notas
```

Nos exercícios 1.x, `validar` solicita uma reflexão e verifica o repositório
no GitHub. No 2.1, coleta os oito artefatos locais. O comando mostra o boletim
e pergunta se deve registrar a nota; `autograde notas` consulta os resultados
oficiais dos envios.

## Referência

[Tutorial do aluno — Autograder IDP-TD](https://github.com/alexlopespereira/idp_governodigital/blob/main/exercicios/tutorial_aluno.md)
