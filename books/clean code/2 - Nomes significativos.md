# Nomes  
  
## Use nomes que revelam seu propósito  
- explicar porque existe;  
- explicar como é usado;  
1. Que tipo de coisas estão na lista?  
2. Qual a importância de um item em uma posição?  
3. Qual a importância de um determinado valor constante  
4. Como eu uso o retorno da função?  
  
## Evite informações erradas  
- não se refira a um grupo de contas como 'accountList' se não for realmente uma lista  
  
## Faça distinções significativas  
- palavras muito comuns são uma forma de distinção ruim (qual a diferença entre Product e ProductData?)  
- Palavras comuns são redundantes  
- Uma variável jamais deve haver a palavra var, uma tabela jamais deve ter a palavra table  
  
## Use nomes pronunciáveis  
- programação é uma atividade social  
```  
    class DtaRcrd102 {        private Date genymdhms;        private Date modymdhms;        private final String pszqint = "102";    }  
        class Customer {  
        private Date generationTimestamp;        private Date modificationTimestamp;        private final String recordId = "102";    }```  
  
## Nomes passíveis de busca  
- nomes longos se sobressaem aos curtos  
- o tamanho de um nome deve ser proporcional ao tamanho do escopo  
  
## Evite codificações  
- nomes não devem ser complexos e codificados  
  
## Não adicione o tipo ao nome da variável  
- a tipagem já é vista na IDE  
  
## Não use prefixos para variáveis  
- tendemos a ignorar o uso de prefixos  
- na maioria das vezes só atrapalham e dificultam a IDE  
  
## Não use decorações demais nos nomes de interfaces  
- pra que usar um IShapeFactory se o tipo de ShapeFactory já é interface?  
- não queremos criar uma **interface** mas sim uma **shape factory**  
  
## Evite mapeamento mental  
- nomes de uma só letra são muito ruins  
> A diferença entre um programador _esperto_ e um programador _profissional_ é que este entende que clareza é fundamental. Ele escreve códigos que outros possam entender.  
  
## Nomes de classes devem ser substantivos  
  
## Nomes de métodos devem ser verbos  
- use get, set, is  
  
## Selecione uma palavra por conceito  
- não use fetch(), retrieve() e get(). Escolha apenas um e mantenha  
- léxico consistente é uma grande vantagem do código  
  
## Não faça trocadilhos  
- evite a mesma palavra para dois propósitos. Usar o mesmo termo para duas ideias diferentes é basicamente um trocadilho  
- não use add() se não estiver nada relacionado com add(). Use append() ou insert()  
  
## Use nomes de domínio  
- programadores sabem o que é um Visitor, uma Queue e um Worker. Serão programadores que lerão seu código  
- use nomes próximos do domínio que você está trabalhando (farmacêutico, alimentício, etc...)  
  
## Nomes com contexto  
- Example2  
  
## Conclusão  
> Programadores acabam ficando com receio de renomear as coisas por temer qeue outros desenvolvedores fiquem contra.  
> Ao melhorar o nome, a codebase fica melhor!