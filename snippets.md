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

git remote set-head <repo> <branch> `Seta qual é a tracking branch default(branch que faz referência ao remote repository)`

### Fast Forward e Merge Commit

git checkout master

git merge <topic_branch> `Fast Forward é a tentativa default de merge`

git branch -d <topic_branch>

#

HEAD `Aponta para o commit atual`

Branch Label `Aponta pro ultimo commit da branch`

Fast Forward `Avança a Branch Label principal para o ultimo commit da topic branch (só possível se não existir commits na branch principal após a criação da topic branch)`

Merge Commit `Combina os commits do topo das duas branchs criando um merge commit que tem os dois topos como pais`
