Disparar ações quando há alguma nova ação no banco de dados.
Quando há mudança nos dados ou eventos no banco de dados.

``` 
	create function returns trigger | event_trigger retorna null
```

roda em background

```
create or replace function log_ator()
returns trigger as $$
begin
update ator
set ultima_atualizacao = now()
where idator = NEW.idator;
return new;
end;
$$ language plpgsql;

```


```
create trigger log_ator after insert on ator

for each row execute procedure log_ator();

```



Quando uma função é executada como uma trigger, algumas variáveis específicas são criadas automaticamente:
- NEW: contém a nova linha do banco de dados para as operações insert e update. Não se aplica a operação DELETE
- OLD: contém a linha antiga do banco de dados para as operações delete e update. Não se aplica a insert.
- TG_NAME: contém uma string com o nome da trigger disparada
- TG_WHEN: contém uma string BEFORE, AFTER or INSTEAD OF, dependendo da definição da trigger.
- TG_LEVEL: contém uma string cnotendo ROW ou STATEMENT, dependendo da definição da trigger
- TG_OP: contém uma string INSERT, UPDATE, DELETE ou TRUNCATE indicando qual operação disparou o trigger.
- TG_RELID: contém o oid (object id) da tabela que gerou o disparo
- TG_TABLE_NAME: contém o nome da tabela que gerou o evento
- TG_TABLE_SCHEMA: contém o nome do esquema
- TG_NARGS: o número de argumentos definidos na declaração CREATE TRIGGER
- TG_ARGV[] retorna a lista de argumentos passados no evento


## Before, instead of, after
- O instante de execução da função pode se dar antes, depois do evento motivador do gatilho
- BEFORE: 
	- A função será executada antes da execução do INSERT/DELETE/UPDATE.
	- A função pode retornar NULL para sinalizar que a operação deve ser pulada
	- Retornando um valor não NULL a operação será executada
	- Para continuar normalmente, deve ser retornado o NEW.
	- Em gatilhos DELETE o valor de NEW será NULL
- AFTER:
	- Será executado depois da operação
- INSTEAD OF
	- Permite usar funções para manipular VIEWS


```
create table emp (
	empname text,
	salary integer,
	last_date timestamp,
	last_user text
)

CREATE TABLE emp_audit(
operation char(1) NOT NULL,
userid text NOT NULL,
empname text NOT NULL,
salary integer,
stamp timestamp NOT NULL
);


CREATE OR REPLACE FUNCTION emp_stamp() RETURNS trigger AS $emp_stamp$
BEGIN
-- Check that empname and salary are given
IF NEW.empname IS NULL THEN
RAISE EXCEPTION 'empname cannot be null';
END IF;
IF NEW.salary IS NULL THEN
RAISE EXCEPTION '% cannot have null salary', NEW.empname;
END IF;
-- Who works for us when they must pay for it?
IF NEW.salary <= 0 THEN
RAISE EXCEPTION '% cannot have a negative or null salary', NEW.empname;
END IF;
-- Remember who changed the payroll when
NEW.last_date := current_timestamp;
NEW.last_user:= current_user;
RETURN NEW;
END;
$emp_stamp$ LANGUAGE plpgsql;

CREATE TRIGGER emp_stamp BEFORE INSERT OR UPDATE ON emp
FOR EACH ROW EXECUTE PROCEDURE emp_stamp();

insert into emp (empname, salary) values ('Juquinha', 10000);
 select * from emp;
 insert into emp (empname, salary) values ('Juquinha2', 2000);
 insert into emp (empname, salary) values ('Juquinha2', 20000);

CREATE OR REPLACE FUNCTION process_emp_audit() RETURNS TRIGGER AS $emp_audit$
BEGIN
--
-- Create a row in emp_audit to reflect the operation performed on emp,
-- make use of the special variable TG_OP to work out the operation.
--
IF (TG_OP = 'DELETE') THEN
INSERT INTO emp_audit SELECT 'D', user, OLD.EMPNAME, OLD.SALARY, now();
RETURN OLD;
ELSIF (TG_OP = 'UPDATE') THEN
INSERT INTO emp_audit SELECT 'U', user, NEW.EMPNAME, NEW.SALARY, now();
RETURN NEW;
ELSIF (TG_OP = 'INSERT') THEN
INSERT INTO emp_audit SELECT 'I', user, NEW.EMPNAME, NEW.SALARY, now();
RETURN NEW;
END IF;
RETURN NULL; -- result is ignored since this is an AFTER trigger
END;
$emp_audit$ LANGUAGE plpgsql;

CREATE TRIGGER emp_audit
AFTER INSERT OR UPDATE OR DELETE
ON emp FOR EACH ROW EXECUTE PROCEDURE process_emp_audit();


insert into emp (empname, salary) values ('Juquinha Segundo',
20000);
select * from emp;
update emp set empname='Juquinha Snaidis' where
empname='Juquinha Segundo';
select *from emp_audit;
delete from emp where empname='Juquinha Snaidis';
select *from emp_audit;
```