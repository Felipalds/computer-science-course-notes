# Gerenciamento de espaços livres
## Bitmap
- Cada bit representa um bloco livre
- Cálculo de blocos livres:
	-```(número de bits por palavra) * (número de 0) + deslocamento até o primeiro bit 1```
- Necessário armazenar os mapas de bis no disco (overhead)

### Lista ligada
![[Screenshot 2024-04-01 at 15.39.36.png]]
- Armazenar apenas o ponteiro do primeiro bloco
- Sem perda de espaço
- Difícil de formatar
- Difícil obter uma sequência de blocos contíguos