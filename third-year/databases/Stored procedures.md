procedimentos armazenados
performance!!!

``` 
create or replace function atores_filmes_caches__(id_ator integer)
returns table (nome text, filme text, cache_ integer)
as 
$$
begin
return query
select a.nome, f.nome, c.cache as cache_ from ator a
inner join filme_ator fa on a.idator=fa.idator
inner join filme f on f.idfilme=fa.idfilme
inner join ator_cache c on a.idator=c.idator
where a.idator=id_ator order by f.nome asc;
end;
$$ language plpgsql;
```

```

create or replace function renomear_ator_nome
(matricula integer, nome_novo text)
returns void as 
$$
begin
update ator set nome = nome_novo
where idator = matricula;
end;
$$
language plpgsql;


```


```
create or replace function buscar_ator(nome_ator text)
returns setof ator as $$
declare id integer;
begin
return query select * from ator where nome like '%'||nome_ator||'%';
end;
$$
language plpgsql;
```

Valor não muda dentro da SP
```
create or replace function buscar_ator(nome_ator text)
returns setof ator as $$
declare id integer;
begin
return query select * from ator where nome like '%'||nome_ator||'%';
end;
$$
language plpgsql;
```


Benefícios:
**reutilizável**: vários usuários e aplicativos podem facilmente usar e reutilizar procedimentos armazenados simplesmente chamando-os

**fácil de modificar**: você pode alterar rapidamente com o comando alter table

**segurança**: os procedimentos aumentam a segurança, restringindo o acesso direto da tabela

**baixo tráfego de rede**: o servidor passa apenas o nome do procedimento e não a consulta toda, reduzindo o tamanho do tráfego da rede

**aumenta o desempenho**: buffer pool para executar mais rapidamente na próxima vez