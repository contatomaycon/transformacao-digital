# Como contribuir

Este repositório reúne os exercícios 1.1 a 1.4 de Transformação Digital.
As contribuições devem manter os exemplos claros e descrever o que foi
efetivamente realizado com Git, GitHub CLI e o agente de codificação.

## Fluxo de uma contribuição

1. Atualize a `main` local com `git pull --ff-only origin main`.
2. Crie uma branch com nome descritivo, como `docs/melhora-explicacao`.
3. Edite os arquivos e confira a alteração com `git diff` e `git diff --check`.
4. Selecione os arquivos com `git add` e registre um commit com mensagem clara.
5. Publique a branch com `git push -u origin NOME-DA-BRANCH`.
6. Abra um PR para a `main` com `gh pr create`, explicando o motivo da mudança
   e a verificação realizada.
7. Revise o conteúdo do PR antes de integrá-lo.
8. Use `gh pr merge --squash --delete-branch` para integrar a contribuição
   em um commit e remover a branch concluída.

## Cuidados com os arquivos

- Mantenha os textos em português e os comandos fáceis de reproduzir.
- Adicione somente os arquivos relacionados à contribuição.
- Preserve alterações locais de outras pessoas.
- Mantenha senhas, tokens e arquivos de autenticação fora do repositório.

## Avaliação das atividades

Execute `autograde validar ID` dentro do repositório, substituindo `ID` por
`1.1`, `1.2`, `1.3` ou `1.4`. Explique os comandos executados na reflexão,
confira o boletim e registre a submissão quando os critérios estiverem atendidos.
Consulte `autograde notas` para confirmar as notas registradas.
