# Explicando o Cherry Pick

O **Cherry pick** é um comando do git que permite escolher commits específicos de uma branch e anexar a outra branch. 

Este é um recurso interessante quando temos equipes que precisam trabalhar de forma concomitante em um mesmo código. Imagine o cenário em que você está trabalhando em uma **branch A** enquanto uma colega está trabalhando em uma **branch B**. 
Em um determinado momento vocês esbarram em um erro que afeta ambas as branchs e é feita a correção na **branch A** mas o trabalho ainda está em andamento e não é possivel realizar o `merge` para propagar as correções. O **cherry pick** será o recurso que permitirá pegar o commit da correção e copia-lo para a **branch B**.

**Importante!!** O uso do **cherry pick** deve ser moderado para evitar duplicação de commits. Sempre que possível utilize o **rebase** ou o **merge** para manter as branchs atualizadas, analisando as particularidades de cada situação para escolher o comando que melhor se encaixa.

### Como realizar um cherry pick em uma branch

O primeiro passo é descobrir o ID do commit que deseja realizar o **cherry picking**.

```bash
$ git checkout branch_feature # indo para branch da feature
$ git log # mostra o log dos commits realizados na branch selecionada

commit f6b178b6a2105718c4980f8c3e71a9d66462f7c8
Author: Letícia Vargas <le.mvargas@gmail.com>
Date:   Wed Oct 20 20:00:07 2021 -0300
```

Depois de copiar o ID do commit, volte para a branch que deseja colar o commit e faça o picking.

```bash
$ git checkout outra_branch  # volta para a branch destino
$ git cherry-pick f6b178b6a2105718c4980f8c3e71a9d66462f7c8  # cherry picking usando o ID do commit desejado
```

### Copiando um intervalo de commits

Caso você precise copiar uma série de commits, o git **cherry pick** permite informar um intervalo de IDs para copiar o grupo de uma vez só. Para isso você deve informar o ID do commit inicial e o ID do commit final. 

Se desejar copiar todos os commits incluindo o primeiro:

```bash
$ git cherry-pick id_inicial^..id_final  # você deve adicionar o acento circunflexo para incluir o commit inicial
```

Mas se o primeiro commit deve ser igorado:

```bash
$ git cherry-pick id_inicial..id_final  # você não precisa adicionar o acento
```

### Principais parâmetros do cherry pick
- `-e` : Permite editar a mensagem do commit.
- `-x` : Adiciona uma mensagem ao commit indicando que é um cherry pick `cherry picked from commit`
- `-allow-empty` : Permite commits em branco (por padrão o cherry pick não permite commits em branco).
- `-allow-empty-message` : Permite commit sem título (por padrão commits sem títulos são barrados).


### E pode ter conflitos?

Sim, podemos esbarrar em conflitos ao realizar o **cheryy picking**. Temos dois caminhos possíveis:

- **Desfaser o cherry pick**: Neste caso você utiliza o comando `$git cherry-pick --abort` para desfazer o cherry pick e voltar a brach ao estado inicial.
- **Resolver os conflitos**: Após a analise e resolução dos conflitos você deve usar o comando `$git cherry-pick --continue` para o git continuar o processo de **cherry picking**

