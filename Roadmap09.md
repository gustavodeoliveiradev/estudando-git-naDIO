# ESTRUTURANDO COMMITS

## Conceitos iniciais sobre estruturação de commits
### Por que é importante:

 - Melhor legibilidade do histórico;
 - Amigável para novos desenvolvedores;
 - Amigável ao versionamento semântico;

**Commits atômicos**
(azul)_iniciando implementação do catálogo de produtos_
(roxo)_Concertando erros de gramática_
(amarelo)_Muda tamanho do mmenu lateral_
(azul)_Adiciona grid de imagens catalogo de produtos_
(azul)_Adiciona CSS catálogo produtos_
(roxo)_Remove estilo do footer_
(verde)_Arruma erro no menu lateral_
(azul)_Finaliza implementação do catálogo de produtos_

O problema dos commits acima antes des serem catalogados com cores é que eles não estavam classificados e assim, se futuramente fossemos revisitar o repositório, haveria um enorme risco de ficarmos perdidos no meio da literal bagunça de commits.
O ideal é que consigamos organizer os commits de uma forma que eles estejam agrupados pra que seja fácil reconhecer o que foi feito em cada agrupamento.

----------

**Português x Inglês**
 - Depende muito do bom senso. E a regra de ouro é seguir o contexto do time mesmo conhecendo as boas práticas.

**ESTRUTURA COMMIT**
_Assunto_ Subject
_Corpo_ Body
_Rodapé_ Footer

**Assunto**
 - Curto e compreensível (quanto menor melhor. Menos é mais aqui);
 - Até 50 caracteres;
 - Começar com letra maiúscula;
 - Não terminar com ponto .;
 - Escrito de forma imperativa: 
    a - _Em inglês use o imperative mood_
        (✓) Add a feature                   (X) Added a feature
        (✓) Modify an existing feature      (X) Modified an existing feature
        (✓) Remove a feature                (X) Removed a feature

    a.a. - _If applied, this commit will ..._
        1. _If applied, this commit will **add** payment integration_
        2. _If applied, this commit will **update** database configurations_
        3. _If applied, this commit will **remove** redundant code_

    b - _Em português use a voz imperativa_
        (✓) Adiciona a funcionalidade x                   (X) Funcionalidade x adicionada
        (✓) Modifica uma funcionalidade existente         (X) Funcionalidade y modificada
        (✓) Remove a funcionalidade y                     (X) Funcionalidade y removida

    b.a. - _Se aceito, esse commit ..._
        1. _Se aceito, esse commit **adiciona** método de pagamento_
        2. _Se aceito, esse commit **atualiza** configurações do banco de dados_
        3. _Se aceito, esse commit **remove** código redundante_

**Corpo**
 - Adicione detalhes ao commit
 - Tente quebrar a linha em 75 caracteres
 - Identifique sua audiência (pra quem você está falando)
 - Explique tudo (escreva como se estivesse escrevendo para leigos)
 - Use markdown

**Rodapé**
 - Referencie assuntos relacionados

 ----------

 Nesse sentido, fizemos abrimos uma issue que são classificadas por # e no commit anterior solucionamos a issue que foi aberta no github.

 ### Commits Semânticos
 #### Conventional Commits

 _Semantic Versioning_
 3 . 2 . 7
 **3** - MAJOR - Toda vez que adicionarmos o que quebra compatibilidade, é uma atualização MAJOR.
 **EXEMPLO** Caso existam outros desenvolvedores trabalhando no mesmo projeto e a sua atualização é tão grande que acaba quebrando a compatibilidade com o projeto dos outros desenvolvedores, ela é chamada de MAJOR
 **2** - MINOR - Nesse caso ela representa uma atualização que não quebra compatibilidade.
 **EXEMPLO** Você sobe uma atualização seja menor ou maior e essa atualização não inviabiliza que os outros desenvolvedores continuem trabalhando em outras versões do mesmo projeto, ou seja, ela não quebra a compatibilidade e por isso é chamada MINOR
 **7** - PATCH - Resoluções de bugs, pequenas alterações do dia a dia que incrementam PATCH. 
 > https://semver.org/

**CONVENTIONAL COMMITS**
    A especificação do Conventional Commits é uma convenção simples para utilizar nas mensagens de commit. Ela define um conjunto de regras para criar um nhistórico de commit explícito, o que facilita a criação de ferramentas automatizadas baseadas na especificação. Esta convenção se encaixa com o SemVer, descrevendo so recursos, correções e modificações que quebram a compatibilidade nas mensagens de commit.
> https://www.conventionalcommits.org/

