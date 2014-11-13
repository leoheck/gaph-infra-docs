
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

Os repositorios sao criados em /var/www/repo, com o comando::

  svnadmin create /var/www/repo/<project-name>
  chown -R daemon:daemon /var/www/repo/<project-name>

Configurando os Acessos
=======================

Editar o arquivo ``/var/www/authz``::

  [groups]
  <project-name>_dev = usuário_1, usuário_2, usuário_3, ...
  <project-name>_user = usuário_a, usuário_b, usuário_c, ...
  
  [<project-name>:/]
  @<project-name>_dev = rw
  @<project-name>_user = r
  @nome_do_repo_user = r
