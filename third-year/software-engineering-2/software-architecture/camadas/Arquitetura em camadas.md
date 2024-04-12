- É um dos mais utilizados desde os anos 60 e 70
- O software é organizado das camadas de maior porte para as de menor porte de forma hierárquica
- Uma camada só pode usar os métodos e serviços de uma camada imediatamente inferior
- Muito usada em aplicações de redes (HTTP -> TCP -> IP -> Ethernet)
	- Modelo OSI
- Fica fácil trocar uma camada por outra (TCP por UDP)
- Fica fácil reusar uma camada (usar a camada de transporte para FTP, SMTP, DHCP...)
- Dikstra 1968

## Modelo de Três Camadas
1. Interface com usuário (exibição, coleta e processamento de informações, cliques, botões)
2. Lógica de negócio (camada de aplicação)
3. Banco de dados

![[Pasted image 20240411143625.png]]
A camada de negócios e banco de dados rodam no servidor, enquanto a camada de interface rodam no cliente.

### Duas camadas
- Junção da interface com a aplicação em uma camada só
- Requer mais poder de processamento do cliente