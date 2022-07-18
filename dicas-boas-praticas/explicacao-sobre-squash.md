# Explicando o Squash Commit

O **squash** é um recurso utilizado para combinar commits. É um comando que tem por objetivo organizar o histórico de commits que pode estar poluído com uma série de pequenos commits realizados ao longo do desenvolvimento.

Com o **squash** mudamos o histórico dos commits agrupando, de uma forma mais significativa, as modificações realizadas.

### Como realizar um squash commit

O **squash** geralmente é realizado em conjunto com o **rebase** (leia mais sobre o rebase [aqui](dicas-boas-praticas/explicação-sobre-rebase.md)). 

```bash
$ git log # listar os commits da branch atual
$ git rebase -interactive HEAD~2  # iniciar o rebase com a opção de interatividade 
```

O argumento `HEAD` referencia o commit mais atual e o `~2` informa ao git que queremos interagir com o segundo commit a partir do mais atual.

Ao executar este comando temos acesso a um aquivo temporário para realização das alterações desejadas. Teremos um arquivo semelhante a este:

```bash
pick 3c71782 Update de contagem  
pick 868bdc9 Adicionado novo parametro 
pick e23462b Opção de excluir parametro  
pick 5c07067 Adicionado modal de erro 

# Rebase 6eaddcd..5c07067 onto 6eaddcd  
#  
# Commands:  
#  p, pick = use commit  
#  r, reword = use commit, but edit the commit message  
#  e, edit = use commit, but stop for amending  
#  s, squash = use commit, but meld into previous commit  
#  f, fixup = like "squash", but discard this commit's log message  
#  x, exec = run command (the rest of the line) using shell  
#  
# These lines can be re-ordered; they are executed from top to bottom.  
#  
# If you remove a line here THAT COMMIT WILL BE LOST.  
#  
# However, if you remove everything, the rebase will be aborted.  
#  
# Note that empty commits are commented out
```

Será apresentada a lista de opções do **rebase** e para o **squash** temos duas opções:

- `squash` : Adiciona no histórico a informação de que foi realizado um squash
- `fixup` : Não adiciona a informação do squash no histórico

O arquivo é aberto no terminal utilizando o `vim`, para interagir com o terminal, digite `i`.

Para realizar o squash basta editar o arquivo adicionando a opção desejada nos commits:


```bash
pick 3c71782 Update de contagem  
squash pick 868bdc9 Adicionado novo parametro 
squash pick e23462b Opção de excluir parametro  
pick 5c07067 Adicionado modal de erro 

```

No exemplo, as linhas dos commits `868bdc9` e `e23462b` foram marcadas como `squash` e serão combinadas ao commit que está logo acima `3c71782`. 

Esse é um ponto importante, o squash sempre irá agrupar os commits com aquele logo acima, ou seja, você sempre irá fazer o **squash** de um commit mais antigo para um mais novo.

Feitas as alterações, basta salvar o arquivo. No terminal você terá a opção de mudar as mensagens dos commits e assim que você salvar o squash estará pronto.

### Squash + merge 

Outra opção é utilizar o **squash** no momento que for realizado o `merge` de uma branch. 

```bash
$ git merge --squash branch_origem # indicar a branch da qual queremos buscar os commits
```

Com este comando o git irá pegar todos os commits da branch informada, realizar um `squash` agrupando tudo em um commit único e então realizar o `merge` da branch.
