## Por que precisamos de um novo compilador?
- nova linguagem
- nova arquitetura

## Definição de uma nova linguagem:
1. Objetivo:
	1. Propósito geral ou específico?
	2. Comercial ou experimental?
2. Paradigma:
	1. Imperativa
	2. Funcional
	3. Lógica
3. Características básicas:
	1. Sistemas de tipos (pelo menos 3 diferentes)
	2. Concorrência/paralelismo
	3. Abstração funcional (não precisamos fazer)
	4. Etc.
4. Nível:
	1. Alto nível, médio nível, assembly? (alto nível)
5. Máquina alvo:
	1. Real/VM
	2. Hipotética
	3. Simulador
6. Tipo do tradutor
	1. compilador (alto nível -> ling.  máquina)
	2. Interpretador
	3. Híbrida
	4. Pré-processador (ling. alto nível est. -> ling. original)
	5. Montador
7. Estrutura
	1. Fases
	2. Forma de integração
	3. Linguagens intermediárias

- NOME:
- SISTEMA DE TIPOS (3 TIPOS)
	- string (ascii com \\0)
	- double
	- int64
- ESTRUTURA DE CONTROLE (SELEÇÃO, LAÇOS)
	- var/rav, main/niam, loop/pool e if/else/fi, 
	- stop, die
	- out, in
- SINTAXE
	- sem chaves
	- tem ponto e virgula
	- sem parenteses no if e while
- OPERAÇÕES
	- recebe: <-
	- a <- 1
	- +, -, \*, /, %, ˆ
	- &, |, !
	- <, <=, >=, >, =, !=




```
var
	a int.
	b int.
	c int.
	d int.
rav

main
	a <- 1.
	b <- 1.

	in d.
	if d < 0 do
		out "Erro mortal \n".
		die.
	fi
		
	loop d > 0 do
		out "Variavel a \n".
		out a.
		c <- a + b.
		a <- b.
		b <- c.
		d <- d - 1.
		
		if d = 1 do
			out "Acabando \n".
			stop.
		or
			out "Não acabando \n".
		fi
	pool
niam

```
