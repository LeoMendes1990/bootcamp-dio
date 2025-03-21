# biblioteca dev
Projeto com java spring boot - JPA.

## Diagrama de Classes

```mermaid
classDiagram
    class Biblioteca {
        +List<Categoria> categorias
    }

    class Categoria {
        +String nome
        +String descricao
        +List<Livro> livros
    }

    class Livro {
        +String titulo
        +String autor
        +String texto
        +String tamanho
    }

    Biblioteca : +categorias
    Categoria : +nome
    Categoria : +descricao
    Categoria : +livros
    Livro : +titulo
    Livro : +autor
    Livro : +texto
    Livro : +tamanho

    Biblioteca "1" --> "many" Categoria : contém
    Categoria "1" --> "many" Livro : contém
