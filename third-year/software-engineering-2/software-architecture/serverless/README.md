# Serverless

## Contexto:
- DDD, Hexagonal, Clean Architecture
    -> Preocupação: modularizar

- Serverless:
    - Evolução da núvem
    
    1. On Premises: configuramos infra, servidor físico e app
    2. Colocation: configuramos servidores físicos e app
    3. Núvens: configuramos servidores virtuais e app
    4. Serverless: configuramos app

    - Tempo ocioso = tempo jogado no lixo
    - Pay as you use

## Funções serverless:
- Invocadas explicitamente ou quando ocorrer um evento
- Stateless (mas podem acessar BDs, filas de mensagens, etc.)
- Tempo de execução máximo (ex: 15 min)
- Funções lambda

- Ex: Netlify


## Arquitetura:
- pequenas funções, que executam rapidamente
- assíncrono

## Vantagens:
- custo pode ser menor
- escalabilidade
- sem configuraçòes

## Desvantagens:
- complexidade arquitetural
- maior latência, principalmente na primeira execução (cold start problem)
- dependência de fornecedores **(vendor lock-in)**
