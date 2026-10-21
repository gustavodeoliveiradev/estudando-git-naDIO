# ALIASES

Aliases são uma forma de dar um apelido para os comandos git:

- ```git config --global alias.s status``` (aqui mudamos o comando git status para apenas s);
- ```git configo --global --list``` (o terminal trará: as configurações... alias.s=status);
- ```git s``` (esse comando agora trará o git status);
- Detalhe: **Podemos fazer isso para todos os comandos**;

_Contudo, é interessante manter os nomes dos comandos no início para adquirir familiaridade._

Para desconfigurar o Aliases:

- ```git config --global --unset alias.s``` (aqui desconfiguramos o 'git s' e voltamos para o 'git status' como normalmente conhecemos);

_O Aliases é uma configuração para garantir agilidade, mas é importante que saibamos cada comando git normalmente antes de configurar um Aliases._
