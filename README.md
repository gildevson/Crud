## Criar Banco de Dados CRUD 2

### Passos:

1. **Criar o Banco de Dados:**
    - Utilize o comando SQL para criar um novo banco de dados. Por exemplo:
        ```sql
        CREATE DATABASE nome_do_banco_de_dados;
        ```

2. **Criar a Tabela:**
    - Utilize o comando SQL para criar uma nova tabela dentro do banco de dados criado. Por exemplo:
        ```sql
        CREATE TABLE nome_da_tabela (
            id INT AUTO_INCREMENT PRIMARY KEY,
            nome VARCHAR(255) NOT NULL,
            email VARCHAR(255) NOT NULL,
            fone VARCHAR(20),
            data_nascimento DATE
        );
        ```
    - Explicação dos campos:
        - `id`: Identificador único da entrada na tabela.
        - `nome`: Nome da pessoa.
        - `email`: Endereço de e-mail da pessoa.
        - `fone`: Número de telefone da pessoa.
        - `data_nascimento`: Data de nascimento da pessoa.

3. **Operações CRUD:**
    - Após a criação da tabela, você pode realizar operações CRUD (Create, Read, Update, Delete) nela para gerenciar os dados conforme necessário.

4. **Exemplo de Operações:**
    - **Criar (Create):**
        ```sql
        INSERT INTO nome_da_tabela (nome, email, fone, data_nascimento) 
        VALUES ('Nome', 'email@example.com', '123456789', '2000-01-01');
        ```
    - **Ler (Read):**
        ```sql
        SELECT * FROM nome_da_tabela;
        ```
    - **Atualizar (Update):**
        ```sql
        UPDATE nome_da_tabela 
        SET nome = 'Novo Nome' 
        WHERE id = 1;
        ```
    - **Deletar (Delete):**
        ```sql
        DELETE FROM nome_da_tabela 
        WHERE id = 1;
        ```

5. **Conectar à Tabela:**
    - Utilize uma linguagem de programação e um driver de banco de dados para conectar-se à tabela e executar as operações CRUD de forma dinâmica.


6. **db.js**
    - import mysql from "mysql"

     ```export const db = mysql.createConnection({
    host: "localhost",
    user: "root",
    password: "1234",
    database: "crud2"
    })  ```
