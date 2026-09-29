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