---
description: 'Exercício para você praticar :)'
---

# Exercício 1

## Proposta

Praticar a adição, commit e push para o GitHub.

## Passos para realização:

### 1. Conteúdo do projeto

1. Crie uma pasta com o nome do projeto \(a sua escolha\) e um arquivo chamado `index.html`
2. Adicione o seguinte conteúdo ao arquivo:

```markup
<!DOCTYPE html>
<html lang="pt-br">
  <head>
    <title>Título da página</title>
    <meta charset="utf-8">
  </head>
  <body>
    <h1>Aqui vai um título</h1>
  </body>
</html>
```

### 2. Subindo seu projeto para o GitHub

1. [Crie um repositório](../git-e-github/setup.md) em seu GitHub
2. Abra o seu terminal de comando e adicione a [origem remota](../ciclo-de-vida-basico/criando-um-repositorio.md) e conecte seu projeto local com o GitHub
3. Verifique as [alterações do seu projeto](../ciclo-de-vida-basico/comandos-mais-utilizados.md#git-status) e [adicione](../ciclo-de-vida-basico/comandos-mais-utilizados.md#git-add) ao fluxo de versionamento
4. Faça um [commit](../ciclo-de-vida-basico/comandos-mais-utilizados.md#git-commit) com uma mensagem útil e na sequência, um [push](../ciclo-de-vida-basico/comandos-mais-utilizados.md#git-push) para o repositório remoto \(GitHub\)

### 3. Lidando com alterações

Abra a pasta do seu projeto, crie uma pasta chamada `imagens`, procure no Google por uma imagem de gato e salve dentro dessa nova pasta. Feito isso, abra seu arquivo `index.html` e adicione as seguintes modificações e salve o arquivo:

```markup
<!DOCTYPE html>
<html lang="pt-br">
  <head>
    <title>Fanpage de Gatinhos</title>
    <meta charset="utf-8">
  </head>
  <body>
    <h1>Perfil #catsoninstagram</h1>
    <img src="images/nome_da_sua_imagem.jpg" />
  </body>
</html>
```

Agora, repita os passos 2 e 3 do [item 2](exercicio-1.md#2-subindo-seu-projeto-para-o-github).  
