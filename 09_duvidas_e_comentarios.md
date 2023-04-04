# 09_duvidas_e_comentarios

Dúvida importância do banco de dados:
É o coração das empresas, com os dados armazenados
é possível tomar decições mais acertivas entendendo
melhor o negócio.

Boas práticas:
Em equipe deve existir sempre uma boa comunicação.
Todos cientes de que algo está sendo executado para
evitar inconsistências.


INNER JOIN:
Utiliza-se para obter um resultado de uma consulta que retorna
dados cruzados entre tabelas de forma que pode se obter apenas
dados desejados

Exemplo:
```sql
FROM public.tb_diretor
INNER JOIN tb_filme
ON tb_filme.id_diretor = tb_diretor.id_diretor;
```

Explain:
Comando para verificar o custo operacional da consulta:
O retorno é um relatorio.
```sql
explain FROM public.tb_diretor
INNER JOIN tb_filme
ON tb_filme.id_diretor = tb_diretor.id_diretor;
```

Conveção snake case:
É padrão usar, mas não é uma regra insclusive é uma
boa prática.

Porquê existem as views temporárias?:
Para obter retorno mais rápidos, mais específicos, etc...
