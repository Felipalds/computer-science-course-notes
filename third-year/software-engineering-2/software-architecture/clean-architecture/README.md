# Clean Architecture
> Mesmo objetivo que a Arquitetura Hexagonal
- Remover tecnologia de domínio
- São círculos
![](../../../../assets/CleanArchitecture.jpg)


## Entities
- Classes que representam objertos importantes do domínio
- Tem vida própria e um identificador
- Podem ser compartilhadas por mais de um sistema
- Exemplos: Livro, Aluno, Professor...

## Casos de Uso
- São classes que implementam os serviços que o sistema oferece
- Fazem todas as validações de regras de negócio
- Não tem relação direta com casos de uso para especificação de requisitos

## Adaptadores
- Mesmo objetivo que os adaptadores de uma arquitetura Hexagonal
- Ligar tecnologias com domínios
- Tecnologias fazem muito mal para o sistema!
- Tecnologia é apenas um detalhe, que muda muito rápido!
- Não pode estar no domínio

## Regra de dependência
