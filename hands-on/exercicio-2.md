# Exercício 2

## Proposta

Em vários casos, você encontrará arquivos que não pertencem \(ou não deveriam\) ao repositório. Exemplos típicos incluem:

* Credenciais \(exemplo: senhas, usuários, keys\)
* Cache de arquivos \(exemplo: .pyc\)
* Ferramentas e bibliotecas complementares para execução do projeto \(exemplo: node\_modules\)

O Git permite que os usuários adicionem um arquivo [`.gitignore`](../ciclo-de-vida-basico/o-que-e-o-.gitignore.md) ao seu projeto, na raiz da pasta, para ignorar esses arquivos específicos.

## Passos para realização:

### Criando um arquivo não rastreável

1. Acesse a pasta do projeto que você criou no exercício 1 e crie um arquivo chamado `minhas_senhas_secretas.txt`
2. Abra o terminal e veja se o arquivo está aparecendo como não rastreado e que pode ser adicionado \([dica](../ciclo-de-vida-basico/comandos-mais-utilizados.md#git-status)\)

### Gerando o .gitignore

1. Crie o arquivo `.gitignore` e salve-o na raiz do projeto \(ele deverá aparecer no mesmo nível dos arquivos `index.html` e da pasta `imagens`\)
2. Abra o arquivo `.gitignore`, digite `minhas_senhas_secretas.txt` e salve-o
3. No terminal, digite novamente o comando para verificar o status dos arquivos e veja que o `minhas_senhas_secretas.txt` não aparece mais!

### Publicando seu .gitignore

No seu terminal, rode os comandos:

1. `git add` para adicionar o arquivo
2. `git commit` para commitar o novo arquivo, sem esquecer de adicionar uma mensagem útil e informativa sobre o que será publicado
3. `git push` para enviar para o repositório no GitHub
