# Modelo de Dados (Diagrama ER)

```mermaid
erDiagram
    USUARIO ||--o{ RECEITA : "cadastra"
    USUARIO ||--o{ FAVORITO : "favorita"
    CATEGORIA ||--o{ RECEITA : "possui"
    RECEITA ||--o{ FAVORITO : "é favoritada em"

    USUARIO {
        int id PK
        string nome
        string email
        string senha
        string cep
        string logradouro
        string bairro
        string cidade
        string uf
    }

    CATEGORIA {
        int id PK
        string nome
        string icone
    }

    RECEITA {
        int id PK
        int usuario_id FK
        int categoria_id FK
        string titulo
        string modo_preparo
        string tempo_preparo
        string url_imagem
        string tags_dieteticas
        string nivel_dificuldade
    }

    FAVORITO {
        int id PK
        int usuario_id FK
        int receita_id FK
        string data_adicao
    }
