## Arquivo
- Espaço contíguo de armazenamento
- Armazenado em dispositivo secundário
### Estrutura
- Nenhuma: sequência de bytes (linguição)
- Registros, documentos, programa executável
- Semântica: SO + aplicação
### Atributos:
- nome
- tipo (em alguns sistemas)
- tamanho
- localização
- dono do arquivo
- proteção
- último acesso
- última alteração
### Operações
- criar
- escrever
- ler
- reposicionar ponteiro do arquivo (FSEEK)
- apagar o arquivo
- truncar o arquivo
- mapeamento do arquivo para a memória
### Nomes e extensões
- É possível ter um tamanho máximo de caracteres (8.3 na FAT)
- Extensões controlam o que podemos fazer com o arquivo (doc, docx, pdf)
	- É um campo opcional, no linux não faz diferença
### Tipo de acesso
#### Sequencial
- Implementação mais simples
- Ponteiro é automaticamente atualizado na leitura
#### Direto
- O arquivo é composto por registros de tamanho fixo
- Operação é realizada **diretamente** em um endereço N

