# Model, View, Controller
- Smalltalk anos 80
![[Pasted image 20240411144608.png]]

- A visão possui botões, cores, textos
- Os controladores tratam e interpretam eventos da visão
- Modelo armazena dados e possuem códigos do domínio da aplicação

### Vantagens:
1. Especialização entre front e back (interface e modelo)
2. Permite que classes de modelo sejam usadas por diferentes views
	 ![[Pasted image 20240411144952.png]]
3. Favorece testabilidade (testar model é mais simples)

> O coração e a parte mais preciosa de MVC está na separação entre código de interface com o usuário (a Visão, também chamada de apresentação) e a lógica do domínio (o Modelo). As classes de apresentação implementam apenas a lógica necessária para lidar com a interface do usuário. Por outro lado, objetos de domínio não incluem código visual, mas apenas lógica de negócios. Isso separa duas partes complexas de sistemas de software em partes que são mais fáceis de se modificar. Também permite várias apresentações da mesma lógica de negócio


![[Pasted image 20240411150024.png]]
 Portanto, a melhor maneira de responder à pergunta é afirmar que existem duas vertentes de sistemas MVC: a vertente clássica, que surgiu com Smalltalk-80 e a vertente Web, que se tornou comum na década de 90 e início dos anos 2000. Essa última vertente lembra bastante sistemas três camadas.