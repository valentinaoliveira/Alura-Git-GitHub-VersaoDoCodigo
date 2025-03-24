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
git switch <nome da branch>: alternar entre branchs
git switch -c <nome da branch nova>: irá criar uma brach nova
git merge <nome da branch>: Irá mesclar o novo com o velho 
git push origin : <nome da branch>: Remove repositório remoto



Site para auxilio
 Ele irá ajudar você a visualizar com o git funciona 

git-school.gihub.io/visualizing-git



No git
Quando você sobe coisa nova na branch, elpa no git irá aparecer o "compare & pull request"
![alt text](image.png)
Que ele irá comparar com a antiga e ele vai entender que em algum momento você irá queuer unir o que foi adicionado com a "main". ão é necessario ir ao site para conseguir fazer o "compare & pull request, é possível fazer pelo proprio terminal o comando é o seguinte: 
git merge <nome da branch>
Irá aparecer "Fast-forward" que significa ele não irá criar um novo commit e não vai fazer nada de diferente, entendendo que a branch raiz está no mesmo lugar que a branch nova

