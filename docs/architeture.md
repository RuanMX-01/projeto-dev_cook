# Arquitetura do Projeto(Architeture.md)

## Descrição Detalhada das Entidades e Atributos

### 1. Entidade: USUARIO (Users)
-Guarda as informações de cadastro e autenticação das pessoas que acessam o sistema.

- **id (Inteiro, Chave Primária): Identificador único do usuário.**

 - **nome (Texto): Nome completo.**

- **email (Texto): E-mail para acesso/login.**

- **senha (Texto): Senha criptografada/validada com (REGEX).**

- **cep, logradouro, bairro, cidade, uf (Texto): Dados do endereço preenchidos via API do ViaCEP.**

### 2. Entidade: CATEGORIA (Categories)
-Guarda as categorias disponíveis para classificação dos pratos.

- **id (Inteiro, Chave Primária): Identificador único da categoria.**

- **nome (Texto): Nome da categoria (ex.: Massas, Sobremesas, Saladas, Bebidas).**

- **icone (Texto): Classe do ícone ou imagem da categoria.**

### 3. Entidade: RECEITA (Recipes)
-Guarda todas as receitas cadastradas pelos usuários no banco fake (db.json do JSON Server).

- **id (Inteiro, Chave Primária): Identificador único da receita.**

- **usuario_id (Inteiro, Chave Estrangeira): ID do usuário autor da receita.**

- **categoria_id (Inteiro, Chave Estrangeira): ID da categoria à qual pertence.**

- **titulo (Texto): Nome do prato.**

- **modo_preparo (Texto): Instruções passo a passo.**

- **tempo_preparo (Texto): Duração formatada por máscara (ex.: 00:45).**

- **url_imagem (Texto): Caminho da imagem (otimizada em WebP).**

- **tags_dieteticas (Texto): Seleção de opções (ex.: Vegano, Sem Glúten, Low-Carb).**

- **nivel_dificuldade (Texto): Opção selecionada em botão de rádio (Fácil, Médio, Difícil).**

### 4. Entidade: FAVORITO (Favorites)
-Associa os usuários às receitas que eles marcaram com estrela (persistido no localStorage do navegador ou via JSON Server).

- **id (Inteiro, Chave Primária): Identificador do registro.**

- **usuario_id (Inteiro, Chave Estrangeira): ID do usuário que favoritou.**

- **receita_id (Inteiro, Chave Estrangeira): ID da receita favoritada.**

- **data_adicao (Texto): Data em que a receita foi gravada nos favoritos.**

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
