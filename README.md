
Configurar Usuário
> $ git config --global user.name "Eduardo Kawassaki"
> $ git config --global user.email "eduardok.fx@gmail.com"

Colorir GIT Bash
> $ git config --global color.ui true

Criar .git
> $ git init

Criar arquivo
> $ touch arquivo.txt

Colocar arquivo no controle de versão
> $ git add arquivo.txt

Colocar todos arquivos no controle de versão
> $ git add .

Status do arquivo
> $ git status

Commit ('-m' de mensagem)
> $ git commit -m "Meu Commit"

Commit 
> $ git commit

Commit ('-a' Commit sem dar o add)
> $ git commit -a  -m "Meu Commit"


LOG 
____________________________________________________

Log
> $ git log

Log Detalhado
> $ git log -p

Log Detalhado 2 últimos
> $ git log -p -2

Log Estatisticas
> $ git log --stat

Log resumido
> $ git log --pretty=oneline
> $ git log --pretty=format:"%h - %an, %ar : %s"

Log 2 dias atrás
> $ git log --since=2.days

Abre o editor
> $ vim teste.php
Ctrl + C (Comando ':wq' para salvar)

Ignore 
____________________________________________________

> $ vim .gitigonre
Arquivo linha a linha > .idea

Remover da lista de commit
____________________________________________________

> $ git reset HEAD teste2.txt

Voltar Versão
____________________________________________________

Pega o Hash
> $ git log

> $ git checkout 21a95384b438bb60699959bfe5568accacfab39f

Voltar commit 
> $ git reset HEAD~2

Volta o arquivo e deixa os arquivos que estava trabalhando
> $ git reset HEAD~2 --soft

 todos arquivos que não existe naquela versão
> $ git reset HEAD~2 --hard



Branches 
____________________________________________________

Lista os brench
> $ git branch

Voltar para master..  '-b' cria novo brench
> $ git checkout -b funcionalidade1

> $ git checkout master

> $ git checkout funcionalidade1

Merge e Rebase 
____________________________________________________

Trás os arquivos para o branch atual
> $ git merge funcionalidade1

Elimina git merge
>$ git rebase funcionalidade1

GitHub 
____________________________________________________

>$ ssh-keygen

Pasta da chave gerada
>$ cd ~/.ssh/

Cola o código no github(setting/ssh)
>$ cat id_rsa.pub

Configurar git
>$ vim .git/config

Subir no Git
>$ git push origin master




Tag
____________________________________________________

Cria Tag
>$ git tag 0.1.0 

Lista tag
>$ git tag -l

Subir tags
>$ git push origin master --tags

Conflito
____________________________________________________

>$ git merge master


Bare
____________________________________________________

Serve apenas como repositório
>$ git init --bare

>$ git remote add local ssh://localhost/arq.git

>$ git checkout master

>$ git push local master


Hook
____________________________________________________


>$ vim post-receive

> # #!/bin/sh
> GIT_WORK_TREE=/Users/eduardo/pasta/meusite.com.br git checkout -f

> $ chmod +x post-receive

> $ cd..

> $ mkdir meusite.com.br

> $ git push local master OU git push origin master



