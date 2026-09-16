# RESOLVENDO CONFLITOS

_Conflitos são comuns quando trabalhamos em versionamento de código, nessa aula vamos entender como são, como encontra-los e como ocorrem._

## COMO ACONTECEM
**SUPOSIÇÃO:** _você tem um código na sua máquina sincronizado com o código do github, em sequida uma outra pessoa copia o código do seu repositório. Logo, vocês fazem modificações no mesmo arquivo e então a edição é feita na mesma linha tanto por você como pela pessoa que copiou o seu código. Logo, o código que está no github é diferente do seu código e diferente do código da pessoa que copiou o seu código._
**OCORRE UM CONFLITE DE MERGE:** _O código em conflito vai ser apresentado pra que você decida qual a versão mais condizente, assim que você decidir, aí sim o repositório do github vai atualizar com a versão escolhida._

```
git push - (envia o código para o repositório)
git pull - (baixa o código do repositório)
git add *
git commit -m "resolve conflitos"
git push origin main
```

**merge conflict** _Quando ele repara que tem uma alteração, o próprio git te avisa pra que você mesmo resolva o conflito. Ao editar o código e resolver o conflito em questão escolhendo como o código deve ficar no repositório remoto, adicionamos e commitamos a resolução do conflito como na amostra acima._