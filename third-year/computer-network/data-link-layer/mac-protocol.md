# MAC and ARP

# MAC (Medium Access Control)
## Intro
- Channel partitioning (time, frequency, code)
- Random access (dynamic)
    - ALOHA, S-ALOHA, CSMA, CSMA/CD
    - CSMA/CD used in Ethernet
- Revezamento
    - Polling do site central, passagem de permissão
    - Bluetooth, FDDI, IBM Token Ring (not used)
    

## Endereçamento MAC
- É um endereço físico
- Função: levar quadro de uma interface para outra interface conectada fisicamente (na mesma rede)
- Endereço MAC de 48 bits (para a maioria das LANs)
- É possível de ser alterado via software
- aa-bb-cc-dd-ee-ff
- FF-FF-FF-FF-FF-FF (não pode ser utilizado)
- Atrelado para cada adaptador de rede (Ethernet/Wi-Fi)
    - Não é por máquina, é por interface

# ARP - Address Resolution Protocol

> Como determinar o endereço MAC sabendo apenas o endereço IP?

- Tabela ARP
- Cada nó IP na LAN está na tabela ARP
- Tabela ARP: mapeamentos de endereço IP/MAC para alguns nós da LAN

```
<endereço IP> ; <endereço MAC> ; <TTL>
```

- TTL (Time to Live): tempo após o qual o mapeamento de endereços será esquecido (normalmente 20 min)
- Perguntando o IP para todas as máquinas. Apenas a máquina responde com o endereço MAC dela
- Usando o broadcast
- Apenas para rede local
- Cada máquina possui sua tabela ARP
- Para redes externas, utiliza-se o roteador
- ARP é plug-and-play
