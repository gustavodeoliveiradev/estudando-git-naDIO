# ENTENDENDO COMO REVERTER COMMITS

## Revertendo commits

 - Existem vários comandos para reverter commits e cada um com uma finalidade específica.
 **IMPORTANTE:** Entender o que cada um faz para não se equivocar e acabar deletando o projeto inteiro sem querer.
---

_git revert_ & _git reset_
Tanto um como outro tem uma forma pra funcionar

**git reset:** Pode ser orientado pelo _hash_ ou _SHA1_ do commit, bem como pela _HEAD_, ou seja, por onde estamos no momento. Além das flags que orientam o comportamento do comando **git reset**
 1. --soft
 2. --mixed
 3. --hard

_EXEMPLO 1._
```
git commit -m "C1"
git commit -m "C2"
git commit -m "C3"
git reset (hash do C1)
```
vai produzir ```Assuming "--hard".```
e a HEAD vai andar para o commit C1 e reverter os commits C2 e C3.

_EXEMPLO 2._
```
git commit -m "C1"
git commit -m "C2"
git commit -m "C3"
git reset HEAD~1
```
Nesse caso, a HEAD vai se mover um commit pra trás ```Assuming "--hard"```
E nesse caso vai reverter o C3, mas se ao invés de HEAD~1, fosse HEAD~2, ele moveria a HEAD 2 commits pra trás e reverteria C3 e C2.

_EXEMPLO 3._
```
git reset --soft HEAD~1
```
Nesse caso, ele volta ao estado dele, antes de serem enviados para o repositório.
O git reset --soft pega os commits que você fez e devolve eles para o staging/index. Fica como se estivessemos acabado de rodar **git add .**

_EXEMPLO 4._
```
git reset --mixed HEAD~1
```
Nesse caso, ele devolve para o working directory. É como se AINDA SEQUER TIVESSEMOS DADO **git add .**.

_EXEMPLO 5._
```
git reset --hard HEAD~1
```
Nessa situação, é recomendado usar o --hard com muito cuidado porque ele exclui o commit, ele não muda o estado do arquivo pra staged ou para o working directory, ele realmente apaga o commit e consequentemente o arquivo que por ventura estivesse sendo commitado antes de envia-lo para o **git push origin main** que é quando enviamos direto para o repositório do github.

---

**git revert**
 - _HEAD~1_
 - _8fs7lxc1_ (exemplo de hash de um commit).

O **git revert** não tem flags, pois ele move o commit orientado pela HEAD ou pela hash do commit em questão. Diferente do **git reset** que tem suas flags.
O **git revert** move a HEAD e reverte o commit em questão gerando um novo commit.
Por exemplo geramos commits "C1", "C2", "C3", "C4" e "C5" e usamos **git revert HEAD~1**. Ele vai gerar um commit novo revertendo o que foi feito no "C4". Portanto, se no C4 foi gerado um novo arquivo, esse arquivo é deletado, contudo, se esse arquivo foi apenas modificado no C4, essa modificação é revertida.