1. Contígua
2. Lista ligada
3. Indexada

## Contígua
- Cada arquivo contém um conjunto de blocos alocados de forma contígua no disco (um em seguida do outro)
- Armazenar apenas o bloco inicial e o número de blocos do arquivo
- Acesso randômico
- Problema: o arquivo não pode crescer!!! 
- Devemos alocar um novo espaço para caber
![[contiguous-fs.png]]

## Lista ligada
- Cada arquivo é composto por uma lista ligada de blocos no disco
- Não precisam ser contíguos
- Armazena apenas o bloco inicial
- No random access!!! (você precisa acessar o bloco anterior para acessar o próximo obrigatoriamente)
![[linked-fs.png]]

## Alocação indexada
- Todos os ponteiros para o arquivo são armazenados em uma tabela
- Acesso **randômico**
- Index Table

![[Screenshot 2024-04-01 at 15.32.12.png]]

![[Screenshot 2024-04-01 at 15.32.44.png]]

![[Screenshot 2024-04-01 at 15.33.16.png]]
