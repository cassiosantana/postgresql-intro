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

Assim que o PgAdmin é aberto ele solicita a senha do usuário postegres para dar acesso aos bancos disponíveis.

A instrutora faz uma breve apresentação da interface e demonstra como abrir o Query tool que basicamente é um arquivo para digitar os comandos SQL, criar a estrutura de dados etc...