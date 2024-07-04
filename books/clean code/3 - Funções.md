## Pequenas
Todas as funções devem ser muito pequenas.
Algo em torno de 20 linhas.

## Blocos e identação
if, switch, for, devem ter apenas uma linha, possivelmente uma chamada de função.

## Fazer apenas uma coisa
> Devem fazer apenas uma coisa, fazê-la bem.

## Um nível de abstração por função
Nível de abstração é o quão alto ou baixo nível é a função. Ela é alto nível? (chamando outras funções, classes, abstraindo muita coisa). Ou baixo nível? (trabalha a nível de strings e bytes).'

## Regra descendente
- Narrativa
- Ler de cima para baixo.

## Switches
- Podemos trocar switches por abstract factories
- Não podemos quebrar o princípio da responsabilidade única
- Não podemos quebrar o princípio aberto-fechado

## Use nomes descritivos
Princípio de Ward: "Você sabe que está criando um código limpo quando cada rotina que você lê é como esperava"
- Metade disso é escolher bons nomes
- Escolha nomes grandes, a IDE autocompleta
- Não tenha medo de alterar, IDEs refatoram para você

## Parâmetros de funções
- A quantidade ideal é zero
- Quanto menos melhor
- Três é o máximo
- Dificulta testabilidade

### Parâmetros booleanos
- Prática horrível
- Mostra que sua função faz mais que uma coisa

## Funções diádes
- ignoramos grande parte dos parâmetros
- não podemos ignorar qualquer parte do código
- são nessas partes em que se esconderão os bugs
- convenção e ordem

### Objetos como parâmetros
- quanto mais parâmetros a sua função precisa, mais provável é de seus parâmetros se juntarem em classes próprias

```
Circle circle (double x, double y, double r);
Circle circle (Point p, double r);
```


## Verbos e palavras chaves
```
boolean assertExpectedEqualsActual(expected, actual)
```

## Evite parâmetros de saída
- altere o estado do objeto em vez disso


## Prefira exceções a retorno de códigos de erro
- Extraia os blocos try/catch
- Tenha uma função com try/catch e outra função sem eles
- Tratamento de erros é uma coisa só, ou seja, a função só deve tratar os erros

```
try 
	doSomething()
catch
	treatError()

doSomething() {

}
```


## Evite repetição
- DRY: Dont Repeat Yourself
- OCP: Open Closed Principle
- A duplicação é a raiz de todo mal do software

## TDD: Test Driven Design
- Sempre faça testes para todas as suas funções