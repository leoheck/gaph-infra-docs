
Administração do SVN
=========================

SVN fica na corfu
/var/www

Arquivos relacionados
/var/www/htpasswd -- armazena os usuarios
/var/www/authz -- contem a configuracao de acesso aos repositorios

Gerenciamento de USUARIOS
==========================

Atualmente os usuarios do SVN nao tem relacao com os usuarios da RODOS

- Criação

``htpasswd /var/www/htpasswd <username>``

- Remoção


Criando Repositorios
====================

Os repositorios sao criados em /var/www/repo, com o comando:

``svnadmin create /var/www/repo``
