### Resumo das Principais Funções em SQL

SQL (Structured Query Language) é uma linguagem padrão para gerenciar e manipular bancos de dados relacionais. Abaixo estão as principais funções e comandos usados em SQL:

#### Criação e Modificação de Estruturas de Banco de Dados

- **CREATE DATABASE**: Cria um novo banco de dados.
    ```sql
    CREATE DATABASE nome_do_banco;
    ```

- **CREATE TABLE**: Cria uma nova tabela no banco de dados.
    ```sql
    CREATE TABLE nome_da_tabela (
        coluna1 TIPO_DADO CONSTRAINTS,
        coluna2 TIPO_DADO CONSTRAINTS,
        ...
    );
    ```

- **ALTER TABLE**: Modifica uma tabela existente.
    ```sql
    ALTER TABLE nome_da_tabela ADD coluna_nova TIPO_DADO;
    ```

- **DROP TABLE**: Deleta uma tabela do banco de dados.
    ```sql
    DROP TABLE nome_da_tabela;
    ```

#### Inserção e Manipulação de Dados

- **INSERT INTO**: Insere novos registros em uma tabela.
    ```sql
    INSERT INTO nome_da_tabela (coluna1, coluna2, ...)
    VALUES (valor1, valor2, ...);
    ```

- **UPDATE**: Atualiza registros existentes em uma tabela.
    ```sql
    UPDATE nome_da_tabela
    SET coluna1 = valor1, coluna2 = valor2, ...
    WHERE condição;
    ```

- **DELETE FROM**: Deleta registros de uma tabela.
    ```sql
    DELETE FROM nome_da_tabela
    WHERE condição;
    ```

#### Consulta e Recuperação de Dados

- **SELECT**: Recupera dados de uma tabela.
    ```sql
    SELECT coluna1, coluna2, ...
    FROM nome_da_tabela
    WHERE condição
    ORDER BY coluna1 ASC|DESC;
    ```

- **JOIN**: Combina registros de duas ou mais tabelas.
    - **INNER JOIN**: Retorna registros que têm correspondências em ambas as tabelas.
        ```sql
        SELECT colunas
        FROM tabela1
        INNER JOIN tabela2 ON tabela1.coluna_comum = tabela2.coluna_comum;
        ```

    - **LEFT JOIN**: Retorna todos os registros da tabela da esquerda e os registros correspondentes da tabela da direita.
        ```sql
        SELECT colunas
        FROM tabela1
        LEFT JOIN tabela2 ON tabela1.coluna_comum = tabela2.coluna_comum;
        ```

    - **RIGHT JOIN**: Retorna todos os registros da tabela da direita e os registros correspondentes da tabela da esquerda.
        ```sql
        SELECT colunas
        FROM tabela1
        RIGHT JOIN tabela2 ON tabela1.coluna_comum = tabela2.coluna_comum;
        ```

    - **FULL JOIN**: Retorna todos os registros quando há uma correspondência em uma das tabelas.
        ```sql
        SELECT colunas
        FROM tabela1
        FULL JOIN tabela2 ON tabela1.coluna_comum = tabela2.coluna_comum;
        ```

#### Filtragem e Ordenação

- **WHERE**: Filtro para selecionar registros que atendem a uma condição.
    ```sql
    SELECT colunas
    FROM nome_da_tabela
    WHERE condição;
    ```

- **ORDER BY**: Ordena os resultados da consulta.
    ```sql
    SELECT colunas
    FROM nome_da_tabela
    ORDER BY coluna1 ASC|DESC;
    ```

- **LIMIT**: Restringe o número de registros retornados.
    ```sql
    SELECT colunas
    FROM nome_da_tabela
    LIMIT número_de_registros;
    ```

#### Funções de Agregação

- **COUNT**: Conta o número de registros.
    ```sql
    SELECT COUNT(*)
    FROM nome_da_tabela;
    ```

- **SUM**: Soma os valores de uma coluna.
    ```sql
    SELECT SUM(coluna)
    FROM nome_da_tabela;
    ```

- **AVG**: Calcula a média dos valores de uma coluna.
    ```sql
    SELECT AVG(coluna)
    FROM nome_da_tabela;
    ```

- **MIN**: Retorna o menor valor de uma coluna.
    ```sql
    SELECT MIN(coluna)
    FROM nome_da_tabela;
    ```

- **MAX**: Retorna o maior valor de uma coluna.
    ```sql
    SELECT MAX(coluna)
    FROM nome_da_tabela;
    ```

#### Funções de Manipulação de String e Data

- **CONCAT**: Concatena duas ou mais strings.
    ```sql
    SELECT CONCAT(coluna1, ' ', coluna2)
    FROM nome_da_tabela;
    ```

- **SUBSTRING**: Extrai uma substring de uma string.
    ```sql
    SELECT SUBSTRING(coluna, início, comprimento)
    FROM nome_da_tabela;
    ```

- **DATE_FORMAT**: Formata uma data em uma string.
    ```sql
    SELECT DATE_FORMAT(data_coluna, '%Y-%m-%d')
    FROM nome_da_tabela;
    ```

#### Exemplos Completos

1. **Criar uma Tabela**
    ```sql
    CREATE TABLE clientes (
        id INT AUTO_INCREMENT PRIMARY KEY,
        nome VARCHAR(100),
        email VARCHAR(100),
        data_cadastro DATE
    );
    ```

2. **Inserir Dados**
    ```sql
    INSERT INTO clientes (nome, email, data_cadastro)
    VALUES ('João Silva', 'joao.silva@example.com', '2024-06-01');
    ```

3. **Atualizar Dados**
    ```sql
    UPDATE clientes
    SET email = 'joao.novoemail@example.com'
    WHERE id = 1;
    ```

4. **Deletar Dados**
    ```sql
    DELETE FROM clientes
    WHERE id = 1;
    ```

5. **Selecionar Dados com Filtragem e Ordenação**
    ```sql
    SELECT nome, email
    FROM clientes
    WHERE data_cadastro > '2024-01-01'
    ORDER BY nome ASC;
    ```

6. **Selecionar Dados com JOIN**
    ```sql
    SELECT pedidos.id, clientes.nome, pedidos.valor_total
    FROM pedidos
    INNER JOIN clientes ON pedidos.cliente_id = clientes.id;
    ```

Esses são os comandos e funções mais importantes em SQL para gerenciar e manipular dados em bancos de dados relacionais.
