- Uma function é um código PL/SQL que pode ser incorporado e invocado sempre que necessário.
- Functions devem possuir nome e com um retorno.
- Sempre retornam valores.
- Aceitam parâmetros
- Podem ser usadas como partes de uma expressão, selects e joins.

Exemplo:
- age (timestamp, timestamp) returns inverval
- current_date
- current_time
- current_timestamp
- now()

```
	select current_date - (400 - 123) // each one is one day
	select age(current_timestamp, current_timestamp);
	select date_part('MINUTE', now())
	select date_part('HOUR', now())


	select to_char((current_date - (31025)), 'Zoz virou chad em DD-MM-YYYY')
```

```
CREATE FUNCTION get_zoz() RETURNS VARCHAR AS $$ BEGIN RETURN 'zoz'; END; $$ LANGUAGE plpgsql;
```


INSERT -> FUNCTION -> DATA

```
create function square5(integer) returns integer as '
	select ($1 ^ (0.5));
' language sql 
immutable
returns null on null input
```


```
create or replace function increment (i integer) returns integer
as $$
begin
return i+1;
end;
$$language plpgsql;
```

## Funções SQL
executam uma lista de declarações SQL retornando o resultado da última query da lista
A primeira linha da última query esrá retornada

Se a última query não retornar nada, será retornado NULL
Para retornar um conjunto de linhas o tipo de retorno deve ser expecificdado como returns set of < TABLE >

nesse caso todas as linhas da última query serão retornadas

## Exemplo

```
CREATE or REPLACE FUNCTION select_alunos(cod_matricula integer) 
returns alunos AS $$
select * from alunos where cod_matricula = $1
$$ language SQL;
```
Aqui vai retornar em uma célula só

```
create or replace function insert_alunos
(idaluno int, nome varchar(100), cod_matricula int)
returns int as $$
with inserido as(
	INSERT INTO ALUNOS(idaluno, nome, cod_matricula)
	VALUES ($1, $2, $3)
	RETURNING cod_matricula
)
select cod_matricula from inserido
$$ language SQL;

// CTE: CONTENT TABLE EXPRESSIONS. É uma tabela temporária para executar.

```

```

create or replace function insert_professor
	(
	nome varchar(255), 
	cod_professor bigint, 
	email varchar(255), 
	telefone varchar(255)
	)
returns varchar(255) as $$
with inserido as (
	INSERT INTO professor(nome, cod_professor, email, telefone) 
	values ($1, $2, $3, $4)
	returning nome
)
select nome from inserido $$
language SQL;

```

```
create or replace function del_prof(cod_professor bigint)
returns void as $$
delete from professor where cod_professor = $1
$$ language SQL


create or replace function get_professor() returns professor as $$
select * from professor
$$ language SQL;
```