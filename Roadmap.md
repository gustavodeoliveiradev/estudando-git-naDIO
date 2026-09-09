# Git & Github

## O QUE VAMOS VER:
> Mudar de pastas
> Listar as pastas
> Criar pastas/ arquivos
> Deletar pastas/ arquivos

### Windows
>> - cd / (change directory - permite navegar entre níveis de pastas)
cd / vai até a raiz (C:)
cd **nome da pasta** acessa a pasta desejada
cd .. volta um nível (sai de uma pasta)
TAB - funciona como um auto-complete
(digitando cd W + **TAB** ele seguramente vai completar **Windows** se estivermos na raiz **C:**)
>> - cls / (clear screen - permite limpar o terminal)
>> - dir / (listar diretorios dentro da pasta onde estamos)
>> - mkdir / (make directory - cria uma pasta)
>> - echo / (imprimir textos, strings, variáveis, depurar ou criar arquivos)
echo hello **devolve o hello**
echo hello > hello.txt **verifica se há um arquivo com esse nome, se não tiver, ele cria o arquivo**
>> - del/rmdir / (delete - arquivos e não pastas / remove directory sim deleta o repositório com arquivos)

**Navegando em pastas:** 
``` 
cd /
dir
cd Windows
cd .. 
cls
echo hello
echo hello > hello.txt
del workspace
echo hello > hello.txt
rmdir workspace /S /Q
``` 

### Unix(Linux ou Apple)
>> - cd / (change directory - permite navegar entre níveis de pastas)
cd / vai até a raiz (C:)
cd **nome da pasta** acessa a pasta desejada
cd .. volta um nível (sai de uma pasta)
>> - clear ou **CTRL + L** (limpa o terminal)
>> - ls / (listar diretorios dentro da pasta onde estamos)
>> - mkdir / (make directory - cria uma pasta)
>> - echo / (imprimir textos, strings, variáveis, depurar ou criar arquivos)
echo hello **devolve o hello**
echo hello > hello.txt **verifica se há um arquivo com esse nome, se não tiver, ele cria o arquivo**
>> - rm -rf / (remove - recursiveforce, apaga todo o repositório, pasta e os arquivos sem perguntar)

**Navegando em pastas:** 
``` 
cd /
ls
cd etc
cd .. 
clear
echo hello
echo hello > hello.txt
rm -rf worspace/
``` 