# AULA 01 MÓDULO 02 - O QUE SÃO BRANCHES

**Branches:** _A palavra significa galho. Quando alteramos qualquer coisa no código mesmo sendo na branch main, já estamos trabalhando com uma **branch**._

**EXEMPLO:** _Estamos trabalhando em uma empresa onde precisamos implementar uma nova funcionalidade na forma de pagamento. Para evitar que os testes dessa nova funcionalidade sejam feitos na **branch** principal, trabalhamos com uma **branch** paralela, criamos a funcionalidade, testamos e caso passe nos testes, essa nova funcionalidade é integrada à **branch main** como vimos no módulo anterior em resolvendo conflitos **merge**._


## O QUE VAMOS APRENDER:

 1. Main x Master (a diferença entre **branch main** e **branch master**);
 2. Navegação em branches;
 3. Criar, Editar, Deletar (localmente);

### MAIN OU MASTER
_São apenas nomes de branches. Durante muito tempo a branch padrão se chamou Master, mas hoje me dia o nome padrão fica a critério de quem tá criando a branch principal. Atualmente, o github está sugerindo um nome main para a branch principal._

**tag HEAD:** _É onde você está, ou seja, onde você está commitando, a branch que você está fazneod commit._

**Branch main:** _É a branch principal do nosso código, a que nomeamos origin._
**PONTO IMPORTANTE:** _As branches geradas de forma paralela para criar novas funcionalidades, testar diferentes ativos para a aplicação, elas são nada mais que uma cópia da branch principal, é como se fossem irmãs da branch principal_

**git merge** _Esse comando, serve para fundir branches. Você vai até a branch que você quer que absorva outra e faz o comando._
**EXEMPLO:** _Criamos uma nova funcionalidade na branch B e queremos adionar essa funcionalidade já testada e aprovada pelo time à branch A(principal). Fazemos um git checkout A e na branch A usamos o comando git merge B._

**Movimentando e criando nova Branch:**
```
git checkout -b nova-funcionalidade <!-- o comando checkout serve para se movimentar, mas também pode gerar novas branches como estamos vendo neste exemplo -->
echo > arquivo2.txt <!-- esse arquivo que criamos está na branch nova-funcionalidade -->
git checkout main <!-- mudamos para a branch main. caso eu passasse -b aí sim estariamos criando uma nova branch, o que não é o que queremos aqui -->
git status <!-- aqui você verá o arquivo2.txt também, porque os arquivos que estão no seu ambiente de trabalho se movem junto com você -->
git checkout nova-funcionalidade
git add * <!-- aqui o arquivo2.txt passa de untracked para staged -->
git commit -m "adiciona arquivo 2 na branch nova" <!-- aqui comitamos o arquivo na nova branch -->
git push origin nova-funcionalidade <!-- guardamos o arquivo2.txt na nova branch -->
git checkout main
git merge nova-funcionalidade
git push origin main
```