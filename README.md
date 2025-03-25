# Comandos Git

## Logs e Histórico de Commits

### `git log --oneline`
Exibe os commits em uma única linha, mostrando apenas os primeiros caracteres do hash e a mensagem do commit. Semelhante ao que é visto no GitHub.

### `git log -p`
Mostra o hash completo, o autor, a mensagem do commit e o diferencial das alterações feitas (diff). Linhas com `-` indicam remoções, enquanto `+` indicam adições.

### `git log --graph`
Mostra uma representação gráfica do histórico de commits, útil para visualizar branches.

### `git log --pretty` ou `git log --format`
Permite personalizar a exibição dos commits. Exemplo:
```sh
git log --format="%H %an"
```
Mostra o hash e o autor de cada commit.

### `git log --help`
Exibe o manual do `git log`, onde é possível encontrar outras opções em "PRETTY FORMATS".

## Visualização de Commits Específicos

### `git show <hash_commit>`
Mostra todos os detalhes de um commit específico, semelhante ao `git log -p`, mas focado em um único commit.

### `git show`
Exibe detalhes do último commit.

### `git show --help`
Exibe a documentação do comando `git show`.

### `HEAD`
Aponta para o último commit realizado.

## Status e Diferenças

### `git status`
Exibe em qual branch você está e quais arquivos foram modificados.

### `git diff`
Mostra a diferença entre o código modificado e o último commit (`HEAD`).

### `git diff <hash_commit>..<hash_commit>`
Compara dois commits específicos.

### `git diff --help`
Exibe a documentação do comando `git diff`.

## Branches

### `git branch`
Lista todas as branches existentes.

### `git branch <nome_da_branch>`
Cria uma nova branch. O nome deve ser simples, sem números ou caracteres especiais.

### `git branch -m <nome_atual> <novo_nome>`
Renomeia uma branch.

### `git branch -d <nome_da_branch>`
Remove uma branch. É necessário sair dela antes de deletá-la.

## Alternando entre Branches

### `git checkout <nome_da_branch>`
Muda para outra branch.

### `git checkout -b <nova_branch>`
Cria uma nova branch e já muda para ela.

### `git checkout -- .`
Desfaz alterações locais nos arquivos.

### `git switch <nome_da_branch>`
Alterna entre branches de maneira mais intuitiva.

### `git switch -c <nova_branch>`
Cria uma nova branch e já muda para ela.

## Merge e Sincronização com o Repositório Remoto

### `git merge <nome_da_branch>`
Faz a fusão de uma branch com outra.

### `git push origin <nome_da_branch>`
Envia a branch para o repositório remoto.

### `git push origin :<nome_da_branch>`
Remove a branch do repositório remoto.

## Stash (Guardar Alterações Temporárias)

### `git stash`
Armazena temporariamente mudanças para retomá-las depois.

### `git stash pop`
Aplica o último stash salvo e o remove da pilha.

### `git stash list`
Lista todas as alterações armazenadas no stash.

### `git stash clear`
Limpa todas as entradas do stash.

### `git stash push -m "<mensagem>"`
Adiciona um nome descritivo ao stash.

### `git stash apply <índice>`
Aplica um stash específico sem removê-lo da lista.

### `git stash drop`
Remove um stash específico da lista.

## Restaurar Alterações

### `git restore`
Desfaz mudanças na área de trabalho ou no stage (equivalente a um "Ctrl+Z" para o código).

### `git restore --staged <arquivo>`
Remove um arquivo da área de stage, sem deletar suas alterações.

### `git restore --source=<hash_commit> <arquivo>`
Restaura um arquivo para o estado de um commit anterior.

## Tags e Releases

### `git tag <nome_da_tag> <hash_commit>`
Cria uma tag para um commit específico.

### `git tag`
Lista todas as tags.

### Annotated Tags
São tags que possuem uma mensagem e um autor.

### `git tag -a <nome_da_tag> -m "<mensagem>"`
Cria uma tag com uma anotação.

### `git push origin <tag>`
Envia uma tag para o repositório remoto.

### `git tag -v <nome_da_tag>`
Exibe detalhes da tag, incluindo commit relacionado, autor e mensagem.

## Cherry-Pick

### `git cherry-pick <hash_commit>`
Aplica um commit específico em outra branch.

## Histórico de Alterações por Autor

### `git blame <arquivo>`
Mostra quem alterou cada linha do arquivo e qual foi o último commit que a modificou.

## Visualizando o Git Graficamente

O site abaixo ajuda a entender visualmente como o Git funciona:

[Git Visualizer](https://git-school.github.io/visualizing-git)

## Pull Requests e Merges

Quando uma nova alteração é enviada para uma branch no GitHub, aparece a opção **"Compare & Pull Request"**.

![Compare & Pull Request](image.png)

Isso indica que, em algum momento, será necessário unir essa alteração à branch principal (`main`). No entanto, essa fusão pode ser feita diretamente pelo terminal com:

```sh
git merge <nome_da_branch>
```

Se a fusão for direta, o Git exibirá "Fast-forward", indicando que a branch principal já está no mesmo ponto da branch a ser mesclada.

## Criando Releases no GitHub

Se for necessário disponibilizar um documento extra, uma descrição específica para a release, ou mesmo um arquivo binário, pode-se criar uma release no GitHub.

![alt text](image-2.png)

Na tela de criação da release:
1. Escolha uma tag.
2. Defina o tipo da release.
3. Adicione uma descrição.
4. Clique em **"Generate release notes"** para gerar automaticamente um resumo das mudanças.
5. Para publicar, clique em **"Publish"**.

