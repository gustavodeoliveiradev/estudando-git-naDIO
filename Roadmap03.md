## AULA 03 PRIMEIROS COMANDOS COM O GIT:

> Iniciar o GIT
> Iniciar o versionamento
> Criar um commit

---

### Comandos
```
#iniciar um repositório git:
git init
#adicionar arquivos para o repositório
git add
#fazer um commit:
git commig -m "conteudo do commit"
```

---

### Markdown: .md
# Título <h1>
## Título <h2>
### Título <h3>
#### Título <h4>
##### Título <h5>
###### Título <h6>

_Itálico_
**Negrito**
```
recipe.md
```

---

## AULA 04 CICLO DE VIDA DOS ARQUIVOS NO GIT

### GIT INIT
**git init cria um repositório no git dentro de uma pasta**

_Tracked_
 - _Unmodified_ o arquivo que ainda não sofreu modificação
 - _Modified_ o arquivo que já sofreu modificação
 - _Staged_ os arquivos que estão se preparando

_Untracked_

### GIT ADD
**preparando os arquivos pra enviar para o repositório**
_Quando um arquivo untracked, recém criado entra direto no staged_
_Quando já temos um arquivo e modificamos esse arquivo, o git percebe pelo SHA1 do arquivo e assim ele muda de **unmodified** para **modified** e se sequencialmente rodamos o **git add** para esse arquivo agora **modified** ele entra em **staged** que é quando ele está preparado para ser **commitado** e subir para o repositório._
 - **git add <arquivo>** _quando queremos adicionar as modificações de um arquivo específico_
 - **git add .** _quando queremos adicionar todas as mudanças feitas no repositório local para o repositório remoto (github)_
 - **git add *** _apenas se quiser adicionar explicitamente os arquivos do nível atual, sendo geralmente menos seguro e prático para controle de versão._


### GIT COMMIT
**quando os arquivos saem de staged e vão para o repositório**
_Assim que ele é **"commitado"** com uma mensagem e enviado para o repositório, é como se dele fosse feito uma foto e essa foto fica guardada no repositório git e assim o arquivo que foi devidamente **"commitado"** passa a ser novamente **unmodified**_

### REPOSITORY
 - **REMOTE REPOSITORY** > seu github, onde você guarda o código e é pra ele que você manda os arquivos quando você faz o passo a passo do **git add** e **git commit**.
 - **AMBIENTE DE DESENVOLVIMENTO** > é a sua máquina, onde você escreve o seu código. Aqui, mesmo que você modifique o código, se você não fizer os comandos git acima, o seu repositório remoto não vai ser modificado.

### GIT STATUS
  - _com o **git status** somos capazes de observar os estágios dos arquivos. Como vimos antes, os arquivos passam por estágios antes de serem **'comitados'** e é através do **git status** que podemos saber em que estágio estão os arquivos do nosso repositório_