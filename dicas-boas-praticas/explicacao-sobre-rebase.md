# Explicando o Rebase

O **Rebase** é um comando do git que permite reorganizar, mover ou combinar uma sequência de commits realizados em um repositório.

Uma boa prática durante o desenvolvimento é a realização de commits a cada atualização funcional, contudo, em alguns casos, ao finalizar uma feature podemos ter um histórico com muitas informações repetidas e até confusas. 

Assim, ao utilizar o **rebase** podemos modificar o histórico do repositório, editando as mensagens, combinando vários commits e até excluindo commits que não são mais necessários no repositório.

O principal motivo para a utilização do **rebase** está relacionado à manutenção de um histórico linear do projeto, com commits significativos que fornecem informações relevantes sobre as features implementadas.

**Importante!!** O **rebase** mexe com toda a estrutura das branchs envolvidas, reescrevendo histórico de commits e unificando informações. Assim, todo processo de rebasing deve ser feito com muito cuidado para evitar perdas ao longo do processo, principalmente se o repositório estiver sendo utilizado por várias pessoas de forma concomitante.

### Como realizar um rebase em uma branch

```bash
$ git checkout branch_feature  # indo para a branch da feature
$ git rebase outra_branch  # fazendo o rebase entre a branch_feature e a outra_branch
```

Com este comando você irá realizar um **rebase** de todos os commits da `outra_branch` em sua branch atual `branch_feature`. 

### Principais comandos do Rebase

- `pick` : Mantem o commit como está, não será alterada a mensagem ou o conteúdo do commit.
- `reword` : Semelhante ao `pick`, mas permite alterar a mensagem do commit.
- `edit` : Permite editar um commit, sendo possível adicionar, alterar e dividir commits.  
- `squash` : Permite combinar commits em um único commit. O squash realiza a combinação sempre com o commit que está acima dele, sendo possível editar a mensagem de descrição.
- `fixup` : Realiza a combinação de commits de forma semelhante ao `squash`, contudo descarta a mensagem do commit que sofre o merge. A mensagem do commit anterior passa a ser utilizada para descrever ambos commits. 
- `exec` : Permite executar comandos shell a cada commit marcado (por exemplo, uma suíte de testes)

### E se surgirem conflitos?

Ao realizar um **rebase** estamos modificando o histórico de commits da branch, logo podemos esbarrar em commits que modificaram um mesmo arquivo. Quando essa situação acontece temos um conflito que o Git precisará de auxílio para resolver.

Caso existam conflitos o Git irá mostrar qual o commit que precisa de atenção. Você terá as seguintes opções:

- **Desfazer o rebase** : Neste caso você deve utilizar o comando `$git rebase --abort` para desfazer completamente o rebase, retornando a branch para o estado anterior ao comando `$git rebase`;
- **Ignorar o commit conflituoso** : Você deve utilizar o comando `$git rebase --skip` para ignorar todas as modificações que estão no commit, ou seja, tudo o que foi realizado neste commit será descartado.
- **Corrigir o conflito** : Neste caso você deve analisar os conflitos, realizar as correções necessárias e ao final usar o comando `$git rebase --continue` para o git continuar o processo de rebase.
