## Termos introdutórios
- **Reconhecimento de padrões**
	- Conceber imagem à alguma coisa
	- Admitir algo como verdadeiro
	- Distinguir certas características
	- Analisar algo detalhadamente
	- É baseado em informações conhecidas (conhecimento prévio)
	- Quanto mais informações conhecidas, mais embasada é a decisão
	![[Screenshot 2024-06-25 at 15.30.01.png]]

	 - Atribuir a um determinado objeto, uma classe, dentre as várias possíveis (classificação)

	Padrão: entidade vagamente definida, que pode assumir um nome
	Classe: conjunto de padrões com características em comum
	Característica ou atributo: uma coluna de um vetor
	Classificação: atribuir classes para as amostras
	Classificadores: utilizados para classificar ou descrever padrões
	Ruído: distorção, falha, imprecisão, outliers.
	
	 
- **Data Mining**
- **Aprendizagem de máquina**

## Sistema de reconhecimento
- ![[Screenshot 2024-06-25 at 15.38.40.png]]
- Aquisição de dados: tirar fotos, retirar exemplares
- Pré-processamento: tratamento e limpeza de dados
- Extração de características: retirar os atributos e características para uma coluna. É uma das mais importantes.

## Treinamento
- Quanto mais robusto e mais tempo, melhor o resultado
- No treinamento, necessariamente precisamos de exemplares de todas as classes
- Manter a proporção de dados

## Aprendizagem de máquina
- Capacitar um modelo/classificador para reconhecer uma nova instância
- Espera-se que seja mais generalista possível
- As características devem ser discriminantes (permitir diferenciar)
- Custo de extração x contribuição no desempenho do classificador
- Classificadores inteiros, floats, enums
	- O tipo da característica influencia na escolha e desempenho do classificador
- Características:
	- Discriminantes (capaz de identificar um objeto)
	- Robustas (capaz de absorver variações dentro de uma classe)
	- Invariantes
	- Possibilidade de conversão em valores (atributo pode ser extraído e convertido em valor)

## Processo de aprendizado
### Aprendizado supervisionado
- Cada registro possui um atributo que identifica a classe (se é gato, se é cachorro; se é fraude ou se não é);
- Tupla X: conjunto de características
- Tupla Y: identifica a classe (uma só)
### Aprendizado não supervisionado
- Não possui a classe que ele pertence


- Bagunçar o máximo possível
- Aleatoriezar (MLP, Perceptrons)