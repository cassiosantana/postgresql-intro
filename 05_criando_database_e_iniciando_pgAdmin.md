Após o psql pelo terminal:

```sh 
Server [localhost]: localhost
Dateabase [postgres]: postgres
Por [5432]: 5432
Username [postgres]: postgres
Password for user postgres: ****
```

Mostar a versão
```sh 
select version();
```

Listar os bancos
```sh
\l
```

Listar os usuários e seus atributos, permissões etc...
```sh
\du
```

Criar tabelas
```sh
CREATE DATABASE catalogo;
```