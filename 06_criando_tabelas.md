# Criando tabelas no Query editor

Comando para criar a tabela tb_diretor
```sql 
CREATE TABLE tb_diretor (
    id_diretor int NOT NULL,
    nome_diretor varchar(50),
    PRIMARY KEY (id_diretor)
);
```
Select simples para obter todos os campos da tabela
```sql
SELECT * FROM tb_diretor;
```

Criando tabela tb_filme
```sql
CREATE TABLE tb_filme (
    id_filme int NOT NULL,
    nome_filme varchar(50),
    id_diretor int NOT NULL,
    id_produtora int NOT NULL,
    gereno varchar(25),
    PRIMARY KEY (id_filme),
    FOREIGN KEY (id_diretor) REFERENCES tb_diretor(id_diretor)
);
```

Select simples para obter todos o campos da tabela
```sql
SELECT * FROM tb_fime;
```