# Processo de aprendizado
### Aprendizado supervisionado
- Cada registro possui um atributo que identifica a classe (se é gato, se é cachorro; se é fraude ou se não é);
- Tupla X: conjunto de características
- Tupla Y: identifica a classe (uma só)
### Aprendizado não supervisionado
- Não possui a classe que ele pertence


- Bagunçar o máximo possível
- Aleatoriezar (MLP, Perceptrons)

- OVA: One versus All
- x contra todas as classes
- y contra todas as classes
- z contra todas as classes



## Avaliação de desempenho
- Acurácia: razão entre o número de acertos pelo número de instâncias
	- Uma porcentagem
- Taxa de erro: razão entre o número de erros pelo número total de instâncias

- Erros têm pesos e custos diferentes
- Acurácia vs custo
	- Quanto melhor acurácia, maior processamento
	- O ganho da acurácia justifica o aumento do custo?

### Hold out
- Dataset de treino x dataset de teste
	- Quantidade de linhas para treinarmos o modelo
	- Quantidade de linhas para testarmos o modelo
	
![[Screenshot 2024-07-01 at 13.47.26.png]]

- A proporção deve ser mantida (estratificação)
	- train_test_split
	- stratify (mantém a proporção)
- Hold-out: proporções para treino/teste
	- 50/50
	- 66/33
	- Treino/teste
	- Adota-se um determinado número de repetições


### Validação
- Podemos também ter um conjunto de validação
![[Screenshot 2024-07-01 at 13.57.19.png]]
- Ajustes de parâmetros e extração de informações
- Hiperparâmetros para calibrar
- Treina, valida, treina valida, para encontrar a melhor configuração.
- Daí jogamos para teste
- Simulado

### Leave one out
- deixar um fora
- estratégia demorada
- inviável

### N-fold cross validation
- validação cruzada
- dividimos em pedaços
![[Screenshot 2024-07-01 at 14.05.41.png]]
- vai separando e usando um fold como teste cada vez
- indicado

### Matriz de confusão
- REAL X PREDITA
- Diagonal principal: acertos
- Acima: predita
- Abaixo: real
- Sabemos qual classe está em conflito com qual
- Podemos dar peso aos erros

- Flexibilização de acertos:
1. Top 1: taxa de reconhecimento
2. Top 2: se a classe estiver nas duas mais prováveis: considera correta
3. Top 3: entre as 3 mais prováveis, considera correta
4. .....
- Não é interessante para problemas onde **não pode errar!**

## Generalização x Overfitting x Underfitting
### Overfitting:
- Treinamos demais que vicia nos dados
- Podemos estabelecer limites
- Erro sobre a validação, perde generalismo e começou a viciar
- Curva de validação x Curva de treino
### Underfitting:
- Treinamos menos do que devia
### Generalização
- Bom parâmetro


## Conhecer os dados
- é algo de extrema importância
- análise descritiva dos dados
- número de instâncias que compõem
- número de atributos, tipos, máximos, mínimos, médias, DP
- quantidade de classes
- distribuições
	- normais
	- tendências
- dados faltantes
	- remover?
	- preencher com média?
- outliers e erros
- dados duplicados