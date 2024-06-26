```
create or replace view alunos_view
as
select nome
from alunos
order by nome asc;

select * from alunos_view;
select * from alunos_view where nome like 'A%';
```

```
create or replace view pedidos_view as
select 
	ped.idpedido as numero_pedido,
	pa.nome as nome_parceiro,
	en.cep as endereco_parceiro,
	tp.descricao as tabela_preco,
	cp.descricao as cond_pag,
	u.nome as nome_user,
	en2.cep as endereco_usuario
from pedido ped
inner join parceiro pa on ped.idparceiro = pa.idparceiro
inner join endereco en on en.idparceiro = pa.idparceiro
inner join tabelapreco tp on tp.idtabelapreco = ped.idtabelapreco
inner join condicaopagamento cp on cp.idcondicaopagamento = ped.idcondicaopagamento
inner join usuario u on u.idusuario = ped.idusuario
inner join endereco en2 on u.idusuario = en2.idusuario;


```