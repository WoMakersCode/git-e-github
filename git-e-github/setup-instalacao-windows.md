# Instalando, configurando e inicializando o Git no Windows


Para instalar o **Git** no Windows, [acesse o site oficial](https://git-scm.com/download/win).

Após baixar o **instalador** execute-o para **começar a instalação**.

![instalador do git](../images/p0001-0.png)

Na primeira tela nos são apresentados os **termos da licença de utilização** do **Git**. 

Basta clicar em **Next**.

![termos de licença](../images/p0001-1.png)

A tela seguinte é sobre o **local de instalação**. Você pode alterá-la, caso queira. Após definir o local da instalação, clique em **Next**.

![local instalação](../images/p0001-2.png)

Na próxima tela, o instalador oferece a possibilidade de selecionar os **componentes** que queremos que sejam instalados. Escolha os **componentes** de sua preferência e clique em **Next**.

Abaixo um exemplo de como prefiro os meus:

![componentes](../images/p0001-3.png)

Em seguida o instalador nos indica que criará uma pasta com **atalhos** no **menu iniciar**. Aqui você pode fazer de acordo com a sua preferência. No meu caso eu deixei o instalador criar os atalhos.

Clique em **Next** para continuar a instalação.

![atalhos](../images/p0001-4.png)

Na sequência, é pedido para selecionarmos o **editor de texto** que deve ser utilizado para editar os conflitos que ocorrerão. Aqui, eu aconselho a instalar seu editor preferido, antes da instalação do **Git** para que o instalador possa encontrá-lo. De todo modo, também é possível fazer a troca posteriormente.

Após a escolha, clique em **Next** para continuar.

![escolhendo editor](../images/p0001-5.png)

Em seguida, o instalador nos pergunta se queremos usar os comandos do **Git**:

- somente no prompt de comandos do próprio git (chamado de Git Bash), neste caso ele não vai alterar a variável de ambiente PATH.

- no **prompt do Windows** neste caso a variável de ambiente PATH será alterada para incluir o caminho onde está o executável do **Git**.

- no prompt do Windows e com os comandos utilitários do Linux. Aqui a variável de ambiente PATH será alterada para incluir o caminho do executável do **Git** e dos executáveis de cada comando utilitário do **Linux**.

Particularmente, prefiro essa última opção, porque o instalador traz para o **Windows** comandos que eu uso muito no terminal do **Linux**, como touch, cat, ls, etc. 

Escolha a opção que acha mais adequada para você e clique em **Next**.

![bash prompt](../images/p0001-6.png)

Na sequência, devemos escolher a biblioteca de **validação de chaves de segurança SSL**. Eu costumo utilizar a **OpenSSL**, que é compatível com outras plataformas.

Em seguida, clique em **Next**.

![SSL](../images/p0001-7.png)

Aqui, o instalador nos pergunta como o **Git** deve tratar o final dos arquivos de texto. **Linux** e **Windows** tratam disso de formas diferentes. De maneira resumida, o **Linux** usa um caractere ASCII para a quebra de linha, enquanto o **Windows** usa dois.

Eu prefiro a primeira opção, para evitar problemas de compatibilidade.

![final arquivo texto](../images/p0001-8.png)

Na próxima tela, o instalador oferece a opção de escolher o emulador de terminal que queremos usar para o **Git**. Particularmente, acho melhor escolher o **MinTTY**, porque ele oferece alguns recursos melhores para terminal.

**Atenção aqui**: se  seu **Windows** for **32 bits** é melhor escolher o **cmd**.

![MinTTY](../images/p0001-9.png)

Na sequência devemos escolher o comportamento padrão de comando **git pull**. Eu preferi deixar marcada a primeira opção.

Em seguida, clique em **Next**.

![git pull](../images/p0001-10.png)

Estamos quase finalizando. Nessa tela temos algumas opções de:

- habilitar **cache de arquivos na memória**. Isso melhora o desempenho do **Git** em alguns casos.

- habilitar o gerenciador de credenciais do **Git**. Isso permite autenticação em duas etapas no **Github**.

- habilitar links simbólicos.

![extras](../images/p0001-11.png)

Por último, o instalador nos oferece alguns componentes que estão em fase de experimentação. Aqui fica totalmente a seu critério. Eu prefiro não instalá-los.

![componentes experimentais](../images/p0001-12.png)

Então, clique em **Install** para começar a instalação.

![instalação](../images/p0001-13.png)

Depois da instalação, já podemos rodar o **Git Bash** e ver o arquivo de texto com as notas da versão lançada.

Para finalizar clique em **Finish**.

![final instalação](../images/p0001-14.png)

Agora você já pode versionar seus códigos no Windows! =D
