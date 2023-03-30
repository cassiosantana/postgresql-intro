# Inserindo valores nas tabelas

Inserindo dados da tabela diretor
```sql
INSERT INTO tb_diretor
VALUES
(1, 'Steven Spilberg'),
(2, 'James Cameron'),
(3, 'Quentin Tarantino');
```

Select para obter os dados da tabela diretor
```sql
select * from tb_diretor
```

Inserindo dados da tabela produtora
```sql
INSERT INTO tb_produtora (id_produtora, nome_produtora) VALUES (1, '20th Century Studios');
INSERT INTO tb_produtora (id_produtora, nome_produtora) VALUES (2, 'Sony Pictures');
INSERT INTO tb_produtora (id_produtora, nome_produtora) VALUES (3, 'Paramount Pictures');
```

Inserindo dados da tabela filme
```sql
INSERT INTO tb_filme
VALUES
(1, 'Django Livre',3,2,'Faroeste/Ação'),
(2, 'Avatar',2,1,'Ficção Científica'),
(3, 'O Resgate do Soldado Ryan',1,3,'Guerra');
```

Select para obter os dados cruzados entre diretor e filme relacionados
```sql
SELECT *
    FROM public.tb_diretor
    INNER JOIN  tb_filme
    ON tb_filme.id_diretor = tb_diretor.id_diretor;
```

### Voltando ao psql

Listar as tabelas
```sh 
\dt
```

Consulta da tablea filme
```sh 
select * from tb_filme;
```