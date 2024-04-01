## Diretórios
Contém informações dos arquivos armazenados em disco
Cada disco ou partição contém uma estrutura de diretórios
### Operações
- Buscar um arquivo
- Criar um arquivo
- Apagar um arquivo
- Listar os arquivos
- Renomear um arquivo
- Verificar o conteúdo do sistema de arquivos
---
-  Eficiência: localizar um arquivo rapidamente
- Nomes: apropriados para usuários
- Agrupamento: arquivos pertencentes a uma mesma aplicação são organizados através dos diretórios

### Um nível:
- Único nível para todos os usuários
- Fácil implementação
- Problemas de conflitos de nomes
![[one-level-fs.png]]

### Dois níveis:
- Cada usuário com seu diretório
- Usuários podem ter o mesmo nome de arquivo
- Nomes de arquivos são compostos pelo **path**
- Busca mais eficiente
![[two-level-fs.png]]

### Em árvore:
- Agrupamento
- Busca mais eficiente
- Conceito de **diretório corrente**
![[in-tree-fs.png]]
- Caminho relativo e absoluto
- Apagar:
	- Arquivo apenas
	- Diretório (remove todos os arquivos e diretórios dentro)

### Grafos acícliclos
![[aciclicos-fs.png]]
- Para diretórios e arquivos compartilhados
- Não ter que copiar o arquivo várias vezes, tem só a referência
	- Breakpointer: apagar todas as referências aos arquivos do sistema