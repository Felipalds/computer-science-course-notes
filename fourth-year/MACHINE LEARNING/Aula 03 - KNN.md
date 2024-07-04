K Nearest Neighbors
Aprendizado mais rápido que tem
![[Screenshot 2024-07-02 at 15.25.24.png]]

Custo de classificação é muito mais alto que o treinamento
- Distância euclidiana para cada membro
![[Screenshot 2024-07-02 at 15.27.43.png]]
Método LAZY!

## Treinamento:
- preguiçoso
- treino rápido, operacional nem tanto
- custo quase todo na classificação
- nem treina, só guarda
- no teste testa com todos

### Distância euclidiana
- usa distância euclidiana
- hipotenusa
![[Screenshot 2024-07-02 at 15.34.03.png]]
- podemos fazer ponderação pela distância ou não
- devemos normalizar os dados

### Distância de Manhattan
- soma dos dois catetos da distância
- para conjuntos discretos
![[Screenshot 2024-07-02 at 15.44.54.png]]


## Como definir um K?
- Regra do cotovelo
![[Screenshot 2024-07-02 at 15.56.54.png]]

### K Pequeno
- Suscetível à ruídos
- 