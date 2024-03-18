# Hexagonal Architecture
> Estabelecer uma separação clara entre domínio (classes do negócio) e restante do sistema
- restante do sistema = banco de dados, telas, coisas menores, outros sistemas, etc.

## Vantagens:
1. Permite que desenvolvedores se concentrem no sistema principal, no domínio
- Representa o propósito do sistema
- Responsável pela geração de valor

2. Testabilidade e qualidade

3. Fácil para trocar de bibliotecas, frameworks, BDs, etc.

## História
- Definida por Alistair Cockburn (anos 90)
- Ideia central: usar Adapters para mediar a comunicação entre domínio e resto do sistema
- Adapters: mesma ideia do padrão de projeto!
- Adaptador nào é domínio, está na fronteira.

![](../../../assets/hex-ports-adapters.svg)

- Cada motivo para se conectar é uma face do hexágono

## Exemplo
> O arquivo principal nada tem haver com tecnologia, apenas domínio (pesquisa mais genérica!)
```
import Adaptadores.PesquisaLivrosWeb;
import Adaptadores.RepositorioImpl;
import Dominio.PesquisaLivrosImpl;

public class Main{
    public static void main(String[] args) {
        RepositorioImpl repo = new RepositorioImpl();
        PesquisLivrosImpl pesq = new PesquisaLivrosImpl(repo);

        new PesquisaLivrosWeb(pesq).start();
    }
}

```

> No caso abaixo, nada há haver com o domínio, apenas tecnologia (adapter com a tecnologia)

```
public class PesquisaLivrosWeb {
    PesquisaLivros pesq;

    public PesquisaLivrosWeb(PesquisaLivros pesq) {
        this.pesq = pesq;
    }

    public void start() {
        staticFiles.location("/templates");

        get("/", (req, res) => {
            res.redirect("index.html");
            return null;
        })
    }
}

```

> Qual é o papel da interface? É a porta de entrada/saída
```
public interface PesquisaLivros {
    String pesquisaPorAutor(String autor);
}
```

> Domínio da pesquisa por autor
```
public class PesquisaLivrosImpl implements PesquisaLivros {
    Repositorio repo;

    public PesquisaLivrosImpl(Repositorio repo) {
        this.repo = repo
    }

    public String pesquisaPorAutor (String autor) {
        return repo.getLivro(autor).getTitulo();
    }
}
```


```
public interface Repositorio {
    public Livro getLivro(String autor);
}
```
> Este repositório precisa ser implementado por alguém! (um adapter)
> Este repositório pode ser um SQL que acessa o banco e retorna o livro pelo autor.
