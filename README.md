Comando 

git log --oneline: vê o id/hash do commit diminuido apenas os primeiros caracteres e a mesagem do commit. Semelhando ao que pode ser visto no gitHub
git log -p: Nele será mostrado o id/hash completo, o autor, mensagem do commit e o diferecial e que será mostrado o "diff" que seria o formato que o git mostra das alterações . Linhas que começam com "-" significa que foram removidas, ja as que estão com "+" foram adicionadas. Possível ver em todos os arquivos 
git log --graph: mostra uma linha linha do log, sendo util pra mostrar as branchs. Ele mostra graficos tambem ao lado esquerdo. 
git log --pretty/ git log --format: exibe o commit da forma que você quiser. Então após digitar o comando é necessario colocar "= "%H %an"", com isso você verá o hash/id do commit e o autor. 
git log --help: Terá o manual e nele você consiguira achar outros formatos de pesquisar o que você quer em "git log --pretty", basta pesquisar "PRETTY FORMATS" que irá encontrar outros formatos especificos. Não é utlizidado  no cotidiano.
git show <hash commit>: irá mostrar tudo do commit, como se fosse "git log -p", mas sedo com um commit em especifico
git show --help: terá a documentação do git show.
HEAD: ultimo commit feito 
git show: irá mostrar os detalhes do ultimo commit
git status: mostra em qual branch voce está logado 
git diff: Mostra diferenca em dois estado, o que foi adicionado e o ultimo commit (HEAD)
git diff --help: Documentação do diff
git diff <hash commit>..<hash commit>: irá mostrar as alteração entre os commits
git branch: mostra as ramificações existentes no trabalho 
git brach -m <nome da branch> <nome novo>: Renomeia o nome da branch 
git branch -d <nome da branch>:  Remove brach, tem que sair da branch para conseguir remove-la
git branch <nome da branch>: você irá criar uma ova branch,porem tem que ser em minusculo, sem umeros, coisa simples
git checkout <nome da branch>: Modifica a branch aonde você está.
git checkout -b <nome da brach nova>: irá criar uma nova branch
git checkout --.: Desfaz alterações 
git switch <nome da branch>: alternar entre branchs
git switch -c <nome da branch nova>: irá criar uma brach nova
git merge <nome da branch>: Irá mesclar o novo com o velho 
git push origin : <nome da branch>: Remove repositório remoto
git stash: Guarda alteração para mexe-lá depois 
git stash pop: Ele aplica o que está na gaveta "git stash" e aplica. Aplicando o ultimo adicionado, metodo pilha 
git stash list: Ele lista tudo o que está no estoque (git stash)
git stash clear : Limpa a lista do stash
git stash push -m "<alguma mensagem>: Assim quando chamar o "git stash list" tera um nome mais discritivo
git stash apply <indice do stash que dejesa trabalhar>: voce consegue mexer no codigo guardado, sem precisar passar pelo ultimo
git stash drop: você pode utilizar ele para remover apenas um item do stash
git restore : desfazer mudanças em arquivos da área de trabalho ou da área de staging "ctrl+z" work tree
git restore --staged <arquivo>: Significa que esta mudando algo dentro dessa stadeg stage area
git restore --source=<hash do commit><arquivo>:vai colocar no estaod que estava antes da alteração de codigoo
git tag <nome da tag><nome do commit>: cria uma tag para esse commit
git tag: ve todas as tags
annotated tags: Uma mensagme para a tag, ela possui mesagem e autor 
git tag -a <nome da tag> -m "": gerar comentario no tag
git push origin <tag>: salvar no remoto a tag
git tag -v <nome da tag>: vai ter para qual commit ela aponta, o tipo, tag, autor e a mensagem dela



Site para auxilio
 Ele irá ajudar você a visualizar com o git funciona 

git-school.gihub.io/visualizing-git



No git
Quando você sobe coisa nova na branch, elpa no git irá aparecer o "compare & pull request"
![alt text](image.png)
Que ele irá comparar com a antiga e ele vai entender que em algum momento você irá queuer unir o que foi adicionado com a "main". ão é necessario ir ao site para conseguir fazer o "compare & pull request, é possível fazer pelo proprio terminal o comando é o seguinte: 
git merge <nome da branch>
Irá aparecer "Fast-forward" que significa ele não irá criar um novo commit e não vai fazer nada de diferente, entendendo que a branch raiz está no mesmo lugar que a branch nova

Release
no git você pode criar uma release 
![alt text](image-1.png)

Ain lea você pode colocar alguma tag 
e se coloca o tipo dela 
voce pode colocar uma descrico nela e pode clicar no botao "Generate release notes"
que ele ira gerar as mudanças feitas e ficara mais facil 
ai para publicare so clicar no "publish"