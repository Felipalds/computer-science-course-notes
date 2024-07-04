![[Screenshot 2024-07-02 at 16.04.37.png]]

- indicada para valores discretos
- robusta à presença de ruídos
- aprendizagem supervisionada
- quanto menor a árvore, mais generalista
- quanto maior, mais específica
![[Screenshot 2024-07-04 at 10.36.10.png]]
- método caixa branca, sabemos como chegou na resposta

## Como achar a raiz da árvore?
- Algoritmo guloso
- "Aprende de cima para baixo"
- Para isso, cada atributo da base é avaliado usando um teste estatístico para saber quão bem ele sozinho classifica os exemplos de treinamento
- Aquele que separar melhor o conjunto de treino é selecionado

## Entropia
- mede o grau de "impureza" em um conjunto de elementos
- quanto mais heterogêneo, maior a entropia
![[Screenshot 2024-07-04 at 10.39.26.png]]![[Screenshot 2024-07-04 at 10.39.43.png]]
- Quanto mais próximo de 1, maior a mistura
- Quanto mais próximo de 0, mais puro o conjunto
- Para se calcular quais serão os atributos raízes, fazemos um cálculo de entropia
![[Screenshot 2024-07-04 at 10.48.10.png]]

## Critério de Gini
![[Screenshot 2024-07-04 at 10.49.56.png]]