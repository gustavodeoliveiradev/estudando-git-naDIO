## AULA 2 O QUE VAMOS VER:
> SHA1
> Objetos fundamentais
> Sistema distribuído
> Segurança

### SHA1:
*A sigla SHA significa **Secure Hash Algorithm (Algoritmo de Hash Seguro),** é um conjunto de funções hash criptográficas projetadas pela **NSA (Agência de Segurnaça Nacional dos EUA)**.*
*Essa encriptação gera um conjunto de 40 caracteres indentificador de 40 digitos.*
*É uma forma curta de representar um arquivo. Se você vai até um arquivo qualquer e muda uma vírgula, ele gera outro código criptogrado de 40 digitos, se você volta e apaga a mudança fazendo com que o arquivo volte a posição anterior, ele devolve o código de 40 digitos anterior*

```
echo "ola mundo" | openssl sha1
SHA1(hello.txt)= f572d396fae9206628714fb2ce00f72e94f2258f
```
Repare no código acima, que qualquer mudança no arquivo, gera um novo código criptografado de 40 caracteres, caso o arquivo volte ao seu estado anterior ao da mudança, o código criptogrado de 40 caracteres anterior volta também. É um mecanismo de controle e segurança do git.

### Objetos fundamentais / Sistema distribuído / Segurança:
**Esse tipo de criptografia da qual falamos no tópico acima, não é feito apenas para arquivos, isso funciona também com objetos:**

> BLOBS - Esse primeiro objeto abordado contém meta dados do git que são tipo do objeto, o tamanho do arquivo, entre outros. A blob é como se fosse o bloco básico de composição. O Blob não guarda o nome do arquivo, ele guarda o sha1 dos arquivos.
> TREES - As Trees armazenam e apontam para tipos de Blobs diferentes. A tree também contém meta dados. A tree também pode apontar para outras trees além dos blobs. As blobs tem um sha1 do arquivo, assim como a tree tem o sha1 da estrutura. É como se tudo estivesse interligado e está.

```
            tree
    README Rakefile | lib
blob        blob        tree
                    simplegit.rb
                        blob
```


> COMMITS - commit aponta pra tree, aponta pro parente, aponta pro autor e aponta pra mensagem. E tem o timestamp que é o momento em que foi feito o commit.. O commit também tem um SHA1 e se você alterar qualquer coisa, ele vai mudar o SHA da tree que vai mudar o SHA do Blob. Por isso é tão seguro.

<table>
    <caption>Commit</caption>
    <tr>
        <td>tree</td>
        <td>s4a5sq1</td>
    </tr>
    <tr>
        <td>parente</td>
        <td>a98acq1</td>
    </tr>
    <tr>
        <td>autor</td>
        <td>quem faz o commit</td>
    </tr>
    <tr>
        <td>mensagem</td>
        <td>"inicia ..."</td>
    </tr>
    <tr>
        <td>timestamp</td>
        <td>...</td>
    </tr>
</table>



## CHAVES SSH E TOKENS
> Chave SSH - é uma forma de manter uma conexão segura com o github, vai ter sempre uma chave pública e uma chave privada. A configuração da máquina com o gihub pra que fique mais seguro.

Comandos Chave SSH:
```
ssh-keygen -t ed25519 -C seu Email github
cd /c/Users/.../.ssh
cat id_ed25519.pub
eval $(ssh-agent -s)
ssh-add id_ed25519
```