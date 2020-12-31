# Exercício 3

## Proposta

Praticar alguns comandos básicos no que diz respeito ao manejo do seu repositório.

## Passos para realização

### 1. Clonando seu repositório

1. No seu perfil do GitHub na aba `Repositories`, crie um novo repositório clicando no botão `New`
2. Se desejar selecione a opção `Add a README file` para criar um arquivo de apresentação
3. Na página do seu repositório copie o link HTTPS ou SSH (se já houver configurado) utilizando o botão code
4. Abra o seu terminal na pasta em que deseja clonar o repositório ou utilize o comando `cd` no terminal pra chegar até lá
5. Utilize o comando `git clone link-HTTPS/SSH` para clonar o seu repositório

### 2. Criando sua nova branch & commit de mudanças

1. No terminal escreva o comando `git checkout -b nome-da-sua-branch` para criar a branch e mudar para ela diretamente
2. Abra o seu editor favorito e faça suas modificações, não se esqueça de salvar! :blue_heart:
3. Voltando para o terminal e dentro da pasta do projeto, use o comando `git add .` para preparar todos os arquivos modificados para o commit
4. Agora use o comando `git commit -m "aqui sua mensagem de commit"` para fazer o commit das suas mudanças na branch
5. Para enviar seu commit para seu repositório remoto utilize o comando `git push origin nome-da-sua-branch`

### 3. Fazendo Pull Request (PR) & dando merge

1. No site do GitHub e na sua página do repositório na aba `Pull requests` clique no botão `New pull request`
2. Agora ajuste nas opções para qual branch você quer enviar as suas modificações (lado esquerdo) e a sua branch que estará enviando essas modificações (lado direito)
3. Observe se não há qualquer conflito, caso não haja confirme a PR!
4. Agora você só precisa fazer o merge, para isso na mesma aba do passo 1, clique na PR que deseja dar merge
5. Como não há nenhum conflito entre as branches (passo 3) é só clicar no botão `Merge pull request`
6. Parabéns, você conseguiu! :tada:
