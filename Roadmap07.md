# VISUALIZAÇÃO DE HISTÓRICO

## Comando stash e seus subcomandos
_Através do seguinte comando, conseguimos visualizar as branches que temos no nosso repositório local e as que empurramos para o repositório do github. No nosso caso, ***main** é a branch que vai aparecer com um * porque é onde estamos trabalhando._
```
git branch
```

---

_Vamos criar uma nova branch para trabalhar, usando o seguinte comando de navegação:_
**IMPORTANTE:** O _git checkout_ serve para navegar entre as branches, mas quando usamos _git checkout -b_ estamos saindo da branch que estamos, criando uma nova branch através da flag _-b_ e navegando até essa nova branch através do _git checkout_.
```
git checkout -b nova-funcionalidade
```

Vamos mudar o nome da branch criada para funcionalidade. Com o próximo comando conseguimos mudar o nome da branch onde estamos que no caso é a branch _nova-funcionalidade_ que passará a ser chamada de apenas _funcionalidade_.
**IMPORTANTE:** O comando a seguir só funciona para mudar o nome da branch onde estamos. Para mudar o nome de uma outra branch onde não estamos, é necessário um outro comando que também vamos estudar a seguir.
```
git branch -m funcionalidade
```

Agora vamos voltar para a branch _main_ de onde vamos mudar o nome da branch _funcionalidade_ através do seguinte comando:
```
git branch -m funcionalidade nova-funcionalidade
```

---

No próximo passo, vamos aprender como deletar uma branch:
```
git branch -d nova-funcionalidade
```

**IMPORTANTE:** _Ao usar o **git checkout** acabamos carregando arquivos de uma branch a outra. No entanto nem sempre é interessante carregar arquivos de uma branch pra testes pra branch principal ou adjascente. Nesse sentido, vamos estudar como navegar de uma branch para outra sem carregar arquivos._
Através do **stash** criamos uma 'caixa' onde guardamos os arquivos da branch e assim limpamos a branch em questão e podemos ir para outra branch usando o **git checkout** sem carregar arquivos e depois voltamos continuar de onde paramos com os arquivos em questão salvos.
```
cd workspace
mkdir teste
cd teste
echo > teste.txt
echo > teste2.txt
git add *
git checkout -b funcionalidade-grande
git stash save "Adicionado arquivos iniciando alteraçoes"
git stash list
git stash pop
git stash clear
```

**IMPORTANTE:** _git stash save ""_ esse comando salva o que estamos fazendo em uma branch para que possamos sair de uma branch para outra sem carregar o que estamos fazendo de uma branch para outra.
Ademais, também vimos que o git _git stash list_ lista o que está no **stash**. O **stash** funciona como um array e lista as **stashs** que temos salvas. Podemos usar o comando _git stash save_ sem mensagem, porém é recomendado que seja escrita uma mensagem para saber o que esta salvo.
O comando _git stash pop_ abre os **stashs** à nossa escolha. Caso tenhamos mais de um, podemos especificar o **stash** desejado para abrir e continuar trabalhando ou também podemos usar o comando _git stash clear_ que abre todos os **stashs**.


---

## Comando git log

_Visualização de histórico:_
De acordo com a atualização do projeto e contando que trabalhamos com diversas outras pessoas, faz-se necessário ter uma visualização do histórico de commits e isso a gente conseguir fazer através do comando **git log**.
```
git log
: q
```
Com esse comando, podemos visualizar os commits feitos no repositório, a hora, a data, quem fez o commit e o sha1 desses commits. E pelo terminal, conseguimos navegar por essas informações usando o mouse ou as setas pra cima e pra baixo ou _PgUp_ ou _PgDn_ no teclado. Se usarmmos _:_ + _q_, saímos da visualização do **git log**. Lembrando que esse é o comando puro do **git log**.

 - Podemos usar o **git log** para visualizar pastas especificas e assim observar os commits só naquela pasta ou diretório específico ou arquivos.
 ```
 git log (nome-da-pasta ou nome-do-arquivo)
 ```

**LEMBRETE:** _ctrl + l_ limpa o terminal


---

## Subcomandos específicos do git log
Podemos trazer a visualização dos logs usando um comando específico do **git log**.
```
git log --oneline
: q
```
Traz o histórico de commits de uma forma resumida.

Também podemos visualizar o histórico de uma outra maneira, com uma linha do tempo praticamente:
```
git log --graph
:q
```

Bem como também podemos visualizar as mudanças de uma maneira gráfica usando **gitk**:
```
gitk
```