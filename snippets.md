# Git Snippets

git log --oneline `Git log reduzido`

git log --graph `Mostra o grafo de commits`

<br/>

git show HEAD^ `Aponta para o primeiro pai do HEAD (sintaxe: ^(primeiro pai), ^^(segundo pai), ^2)`

git show HEAD~ `Aponta para o pai do commit (sintaxe: ~(pai), ~~(avô), ~2)`

<br/>

git checkout -b <branch_name> `Cria uma nova branch e altera o HEAD para ela`

git reflog `Retorna uma lista de alterações no HEAD`

<br/>

git remote set-head <repo_name> <branch_name> `Seta qual é a tracking branch default(branch que faz referência ao remote repository)`

<br/>

git commit --amend -m <\_msg> `Reescreve a mensagem de commit`

git commit --amend `Adiciona arquivos no ultimo commit já existente`

git commit --amend --no-edit `Faz o mesmo que o comando anterior mas mantem a mensagem de commit`

### Fast Forward e Merge Commit

git checkout master

git merge <topic_branch> `Fast Forward é a tentativa default de merge`

git branch -d <topic_branch>

### Rebase

git checkout featureX

git rebase master

#Equivalente a:

git rebase master featureX `Git põe a master como novo pai da featureX`

Em caso de conflito, resolver o conflito, adicionar na staging os novos arquivos e rodar:

git rebase --continue

### Rebase interativo

git rebase -i <start_commit> `Executa o rebase interativo, libera o acesso a todos os commits filhos do start_commit`

`O rebase interativo nos permite editar toda a história dos commits(arquivos, commit messages, etc) afim de resolver quaisqueres erros`

### Squash Merge

git merge --squash <topic_branch>

`Faz um squash em todos os commits da topic_branch e da um merge colocando como ultimo commit da branch atual, esse merge mantem a linearidade e não exclui nem altera a topic_branch`

#

HEAD `Aponta para o commit atual`

Branch Label `Aponta pro ultimo commit da branch`

Topic Branch `Branchs de alguma feature, bug, hotfix, etc`

Base Branch(long Lived Branch) `Branchs de longa vida`

Tracking Branch `Branch do repositório remoto representada no repositório local`

Fast Forward `Avança a Branch Label principal para o ultimo commit da topic branch (só possível se não existir commits na branch principal após a criação da topic branch)`

Merge Commit `Combina os commits do topo das duas branchs criando um merge commit que tem os dois topos como pais`

Rebase `Rebase é uma forma de merge na qual você insere novos commits como pais dos próximos commits da sua branch atual mudando toda a história do projeto (Perigoso)`

squash `Squash junta o commit mais novo com o mais antigo criando um único commit contendo os dois commits`
