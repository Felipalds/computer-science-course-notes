# Logs/Journaling
- Cada atualização no sistema de arquivos é armazenada em um arquivo de transação (logs)
	- Uma atualização é considerada aceita quando escrita no arquivo de logs
	- O sistema de arquivos não necessariamente está atualizado
- Transações processadas assincronamente
- Se um sistema é reiniciado, as transações são efetuadas antes do sistema voltar a ser utilizado
- Duas escritas são necessárias: no log e no FS de fato

## EXT3
> Journaling pode ser configurado de três modos distintos:
1. Journaling
2. Ordered
3. WriteBack