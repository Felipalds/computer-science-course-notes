# Análise assintótica
- permite estimar o custo para se estimar o custo de determinado algoritmo
- Custo é chamado de custo computacional, custo assintótico ou complexidade assintótica
## Critérios comuns:
- Número de operações básicas
- Número de comparações
- Número de indexações
- Número de acesso a disco
- Número de swaps
- Espaço em memória
- Número de acessos a servidor

> A análise assintótica de algoritmos ignora problemas pequenos e concentra-se em problemas cujos valores tendem a ser extremamente grandes

Exemplo:
nˆ2, 3nˆ2/2, 9999nˆ2, nˆ2/1000
- neste exemplo, todos tem a mesma complexidade! apenas o nˆ2 que importa.

## Ordem Big O
- Representa o teto de custo do algoritmo, o pior caso.
- Trata-se de funções assintoticamente não negativas, ou seja, funções f tais que f(n) >= 0 para todo n suficientemente grande
- Explicitamente: f é assintoticamente não negativa se existe um inteiro n0 tal que f(n) >= para todo n>=n0
- O maior elemento sempre deve ser positivo

### Propriedades:


## Ordem ozinho
- O pequeno, (ômicron)
- Não permite que as duas funções se toquem

## Ordem ômega
- Limite inferior
- Custo mínimo
- É o menor custo de execução de um algoritmo

## Ordem ômegazinho
- Não permite que ambas as funções chegam iguais

## Ordem teta
- Mesmo comportamento
- QuickSort = teta(MergeSort)

### Análise assintótica:
- Provê uma aproximação do real custo de execução do algoritmo
- Porém, não é necessario implementar e rodar o algoritmo para avaliar o custo
- Basta fazer a análise de forma precisa


# Análise empírica
- cenário
- variações


