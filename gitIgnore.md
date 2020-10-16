### GitIgnore

Um arquivo ".gitignore" é um arquivo utilizado pelo git para ignorar alguns arquivos no momento que for definir quais arquivos ele observa.
Desta forma, qualquer arquivo ou padrão definido dentro deste arquivo será invisível ao git e não será afetado por git add ou git commit. A sintaxe é bastante simples e temos somente que definir em cada linha, o nome ou padrão a ser ignorado.

Exemplo A:
```
readme.md
code.py
src/
outputs/
```
Se criamos um arquivo com o nome ".gitignore" e adicionamos a pasta principal do repositório com o Exemplo A escrito nele, os arquivos readme.md e code.py e os diretórios src/ e outputs/ serão ignorados

Isto é muito útil para não lotarmos os repositórios com arquivos desnecessários ou temporários como por exemplo objetos criados por compiladores.

Exemplo B:
```
*.o
*.txt
```
O "\*" é um caracter especial que significa "qualquer coisa". Este é um exemplo de um padrão que pode ser feito, no qual todos os arquivos que terminem em ".o" ou ".txt" serão ignorados pelo git.