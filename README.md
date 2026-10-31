# Transformação Digital

Repositório dos exercícios 1.1 a 1.4 da disciplina de Transformação Digital.

As atividades praticam versionamento com Git, colaboração pelo GitHub,
uso do GitHub CLI (`gh`) e automação com um agente de codificação.

## Sobre

Atividades de Maycon Douglas, da turma TD-2026-03.

Este mesmo repositório será usado nos quatro exercícios. Ele foi criado
previamente pelo aluno; o agente auxilia na preparação dos arquivos, no clone
adicional, na colaboração por pull requests e na avaliação pelo autograder.

No Git, `git add` prepara as alterações, `git commit` registra uma versão no
histórico local e `git push` envia os commits para o repositório no GitHub.

## Atividades

| Exercício | Prática |
| --- | --- |
| 1.1 | README, dois commits e publicação no GitHub |
| 1.2 | Autenticação no `gh`, branch, pull request e merge |
| 1.3 | Consulta e clone deste repositório com auxílio do agente |
| 1.4 | Criação de `CONTRIBUINDO.md` em uma branch e integração por PR |

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
autograde notas
```

O comando `validar` solicita uma reflexão, mostra o boletim e pergunta se deve
registrar a nota. As evidências do repositório são verificadas no GitHub, por
isso as alterações precisam estar publicadas com `git push`.

## Referência

[Tutorial do aluno — Autograder IDP-TD](https://github.com/alexlopespereira/idp_governodigital/blob/main/exercicios/tutorial_aluno.md)
