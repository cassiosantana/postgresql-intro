# Instalação do postgreSQL no Ubuntu

Basicamente é só seguir as orientações do site oficial para o SO desejado. No caso será para o Ubuntu.
https://www.postgresql.org/download/linux/ubuntu/

Para ver o cluster
```sh
pg_lsclusters
```
## Configuração de SUPERUSUARIO

Logar com o usuário postgres
```sh
sudo -i -u postgres
```

Entrar no utilitário psql do PostgreSQL
```sh
psql
```
Agora podemos configurar o super usuário
```sh
\password
```

Agora precisamos encontrar o arquivo pg_hba.conf
Digitar no psql:
```sh
show hba_file;
```

Após ser mostrado o endereço do arquivo devemos saír do psql
```sh
\q
```

```sh
exit;
```

O local na minha máquina onde o arquivo estava localizado foi:
/etc/postgresql/15/main/pg_hba.conf

Comando para editar o arquivo
```sh
sudo nano /etc/postgresql/15/main/pg_hba.conf
```

Perto do final do arquivo deve conter uma linha que tem que ser editada para ficar desta forma

>Database administrative login by Unix domain socket
>local   all             postgres                         md5 

Depos de salvar,
```sh
sudo systemctl restart postgresql
```

Agora é possível fazer login da forma correta com o comando:
```sh
psql -U postgres
```

Agora, dentro do psql é possível também criar um novo usuario e que inclusive, caso necessário, sendo um super usuário como o postgres:
```sh
CREATE USER nome_do_usuario WITH PASSWORD 'senha_do_usuario' SUPERUSER;
```
Caso não deseje que o novo usuário não seja um super usuário basta remover o 'SUPERUSER' do comando.

Posteriormente será possível fazer login com este novo usuário com este comando:
```
psql -U nome_do_usuario -d postgres
```
> A flag -d postgres indica que o usuário estará se conectando ao banco de dados postgres. Se a flag não for passada no comando o usuário tentará ser logado em um banco com seu mesmo nome e caso o mesmo não exista teremos um erro.

Caso não se lembre do usuário utilizado para se logar basta digitar:
```
\conninfo
```

## Agora a instalação do pgadmin
Seguir as instruções do site oficial
https://www.pgadmin.org/download/pgadmin-4-apt/

