# Microsservices



## Desvantagens
- maior complexidade, pois são **aplicações distribuidas**
- mais difícil:
    - monitoramento
    - testes e integração de sistemas
    - garantia de atomicidade em transações (garantir que a transação ocorreu nos dois ou mais microsserviços)

### Transações distribuidas
> Atomicidade é uma propriedade chave de transações
- Ou tudo, ou nada
- Resultados intermediários não são visíveis

1. Banco de dados centralizado:
```
try {
    op1();
    op2();
    commit();
} catch(e) {
    rollback(e);
}
```

2. Banco de dados distribuidos
- Two Phase Commit (2PC)
    - Algoritmo para atomicidade de transações distribuídas
    - Problemas conhecidos, incluindo latência e impasses
    - Não é recomendado na prática
    - Redes, pacotes, ACK, ordem, TCP...

- Sagas (1987)
    - Dois conjuntos, um de transações e outro de compensações (rollbacks)
    - Uma transação de crédito é compensada por outra de débito, é como um undo
    - Caso uma transação falhe, todas devem ser compensadas, com rollback









