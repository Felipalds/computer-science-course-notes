# Logs/Journaling
- Cada atualização no sistema de arquivos é armazenada em um arquivo de transação (logs)
	- Uma atualização é considerada aceita quando escrita no arquivo de logs
	- O sistema de arquivos não necessariamente está atualizado
- Transações processadas assincronamente
- Se um sistema é reiniciado, as transações são efetuadas antes do sistema voltar a ser utilizado
- Duas escritas são necessárias: no log e no FS de fato

## EXT3
> Journaling pode ser configurado de três modos distintos:
1. Journal
	- Journal armazena no arquivo de log os dados e metadados (diretórios e informações sobre o arquivo) no arquivo de log
	- Duas escritas
2. Ordered
	- As atualizações no conteúdo do arquivo são armazenados diretamente no sistema de arquivos. Os metadados são escritos em definitivo depois da escrita do conteúdo do arquivo
3. WriteBack
	- As atualizações nos metadados e nos arquivos são realizados de forma assíncrona