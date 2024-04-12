# Protocolo ARP 
> Address resolution protocol 
- RFC 826 (1982)
- Usado para resolução de endereços (conversão) da camada de rede em endereços da camada de enlace
- O ARP mapeia um endereço de rede (IPv4 por exemplo) em um endereço Ethernet ou MAC

## Como funciona?
1. A requisição é enviada via Broadcast, solicitando o endereço MAC de uma determinada máquina através do endereço IP.
2. A resposta é enviada de forma Unicast.
3. Ambos os intervenientes guardam os dados um do outro em uma cache

- É sempre para redes locais, nunca entre redes