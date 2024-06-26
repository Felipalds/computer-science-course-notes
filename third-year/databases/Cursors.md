Unbound: todo acesso se dá por meio de uma variável de cursor.
Bound: declaração é ligada diretamente uma query

Para ter acesso ao cursor é necessário declarar uma variável.

O postgresql provê um tipo especial  - refcursor
a variável pode ser usada em qualquer query

DECLARE meu_cursos REFCURSOR;

DECLARE cur_filme CURSOR FOR SELECT * FROM filme;


pedir quais slides
pedir qual livro


EXEMPLO:

```
CREATE OR REPLACE FUNCTION refAlunos() RETURNS VOID AS $$
DECLARE
	exemplo_cursor_alunos CURSOR FOR SELECT * FROM alunos2;
	aluno2 alunos2%ROWTYPE;
BEGIN
	OPEN exemplo_cursor_alunos;
	-- Loop para percorrer os registros

	LOOP
		FETCH exemplo_cursor_alunos INTO aluno2;
		EXIT WHEN NOT FOUND;'
		-- Exibir o nome do aluno

		RAISE NOTICE 'Nome: %', aluno2.nom_alu;
	END LOOP;
	CLOSE exemplo_cursos_alunos;
END;

$$ LANGUAGE plpgsql


BEGIN;
SELECT refAlunos();
COMMIT;

```