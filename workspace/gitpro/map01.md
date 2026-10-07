# GIT E GITHUB FOCADO EM PULLREQUEST

## O que podemos esperar desse módulo ?
 - **Forks**
 - **Permissões**
 - **Templates de issues e Pull Request**
 - **Meu primeiro Pull Request**
 - **Aliases**

formato: 'https://github.com/userName/repositoryName'

exemplo: 'https://github.com/Perkles/livro-receitas' **fork** 
         'https://github.com/outraPessoa/livro-receitas'
Para fazer alterações, precisamos puxar o repositório para o nosso perfil fazendo um **Fork**.
Assim, logo que o **fork** for feito, podemos alterar esse projeto em um repositório no nosso perfil
 1. Após fazer o **Fork**, o repositório fica ligado ao antigo.
 2. (importante criar uma nova branch específica para fazer modificações ao repositório forkado, pois isso facilita à pessoa que estará avaliando o seu **Pull request**).
 ``` git checkout -b adiciona-nova-receita ``` (é importante também seguirmos as boas práticas e nomear a branch fazendo referência direta ao objetivo).
 ``` git add * ```
 ``` git commit -m "Adiciona nova receita salada.md" ```
 ``` git push origin adiciona-nova-receita ```
 3. O próprio git da a opção de fazer um pull request. (É importante adicionar uma boa descrição para o pull request).