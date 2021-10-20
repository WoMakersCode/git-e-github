# Instalando, configurando e inicializando o Git no Linux


Para instalar o Git no Linux, digite no terminal:

```
$ sudo apt install git
```

- **$** indica que você deve usar o **usuário comum** para fazer essa operação.

- **sudo** é o comando que dá permissões de super usuário temporariamente; assim é possível fazer a instalação de programas.

- **apt** do inglês, *Advanced Package Tool*, em português, Ferramenta de Empacotamento Avançada; é a ferramenta que nos ajuda na instalação, atualização e desinstalação de programas, entre outras funções.

- **install** é o comando de instalar, indicando ao apt o que fazer.

Verifique se a instalação foi feita corretamente digitando:

```
$ git --version
```

Você receberá o retorno da versão instalada.

Antes de começar a usá-lo é preciso fazer as configurações iniciais. Assim,

```
$ git config --global user.name <seu_nome_aqui>
```

- Digite seu nome sem os sinais de < e >.

Em seguida:

```
$ git config --global user.email <seu@email.com>
```

- Digite seu email sem os sinais de < e >.

Configurando o editor padrão:

```
$ git config --global core.editor nano
```

No meu caso, estou usando o **nano**, mas você pode utilizar outro de sua preferência.

Para verificar as suas configurações:

```
$ git config --list
```

Caso queira que as configurações sejam feitas apenas no diretório (não global) indicado, basta retirar dos comandos a flag **--global**. Assim:

```
$ git config user.name <seu_nome_aqui>
$ git config user.email <seu@email.com>
$ git config core.editor nano
```

Para inicializar o git no diretório desejado (caso ainda não o tenha feito), vá até o local onde você deseja fazer o controle de versionamento.

```
$ cd /home/seu_usuário/seu_repositório
```

- **cd** do inglês, change directory; serve para mudar de diretório/pasta.

e digite

```
$ git init
```

A partir de agora, os arquivos serão rastreados pelo **Git**.
