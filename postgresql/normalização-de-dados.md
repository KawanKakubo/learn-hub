### Normalização de Dados

A normalização de dados é um processo utilizado no design de bancos de dados relacionais para minimizar a redundância e dependência de dados. Esse processo organiza os dados em tabelas e colunas de modo a reduzir a duplicação e garantir a integridade dos dados.

#### Objetivos da Normalização

1. **Eliminar Redundância de Dados**: Reduz a duplicação de dados, o que economiza espaço e facilita a manutenção.
2. **Assegurar a Integridade dos Dados**: Garante que as dependências de dados são lógicas e consistentes.
3. **Melhorar a Flexibilidade**: Facilita a adaptação do banco de dados a novas necessidades sem comprometer a estrutura existente.

#### Formas Normais

A normalização é geralmente realizada em várias etapas conhecidas como formas normais. Cada forma normal (FN) possui critérios específicos que devem ser atendidos.

1. **Primeira Forma Normal (1NF)**
   - **Critérios**: Elimina grupos repetitivos, assegura que cada campo contém apenas um valor e cada registro é único.
   - **Exemplo**: Transformar uma tabela que armazena múltiplos valores em uma única coluna em várias linhas.

   ```sql
   -- Antes da 1NF
   CREATE TABLE Cliente (
       id INT,
       nome VARCHAR(100),
       telefones VARCHAR(100) -- armazena múltiplos telefones como "123456,789012"
   );

   -- Depois da 1NF
   CREATE TABLE Cliente (
       id INT,
       nome VARCHAR(100)
   );

   CREATE TABLE ClienteTelefone (
       cliente_id INT,
       telefone VARCHAR(20),
       PRIMARY KEY (cliente_id, telefone)
   );
   ```

2. **Segunda Forma Normal (2NF)**
   - **Critérios**: Atende a 1NF e todos os campos não-chave dependem da chave primária.
   - **Exemplo**: Eliminar dependências parciais, onde um campo depende apenas de uma parte da chave composta.

   ```sql
   -- Antes da 2NF
   CREATE TABLE Pedido (
       pedido_id INT,
       produto_id INT,
       quantidade INT,
       produto_nome VARCHAR(100) -- depende apenas de produto_id
   );

   -- Depois da 2NF
   CREATE TABLE Pedido (
       pedido_id INT,
       produto_id INT,
       quantidade INT
   );

   CREATE TABLE Produto (
       produto_id INT,
       nome VARCHAR(100)
   );
   ```

3. **Terceira Forma Normal (3NF)**
   - **Critérios**: Atende a 2NF e todos os campos não-chave dependem diretamente da chave primária.
   - **Exemplo**: Eliminar dependências transitivas, onde um campo depende de outro campo que não é a chave primária.

   ```sql
   -- Antes da 3NF
   CREATE TABLE Cliente (
       cliente_id INT,
       nome VARCHAR(100),
       cidade VARCHAR(100),
       estado VARCHAR(2),
       estado_nome VARCHAR(100) -- depende de estado, não diretamente da chave primária
   );

   -- Depois da 3NF
   CREATE TABLE Cliente (
       cliente_id INT,
       nome VARCHAR(100),
       cidade VARCHAR(100),
       estado VARCHAR(2)
   );

   CREATE TABLE Estado (
       estado VARCHAR(2),
       nome VARCHAR(100)
   );
   ```

4. **Forma Normal de Boyce-Codd (BCNF)**
   - **Critérios**: Atende a 3NF e, para cada dependência funcional, o lado esquerdo é uma chave candidata.
   - **Exemplo**: Eliminar anomalias causadas por dependências funcionais complexas.

#### Considerações Adicionais

- **Desnormalização**: Embora a normalização seja importante para evitar redundâncias e manter a integridade dos dados, em algumas situações, pode ser necessário desnormalizar dados para melhorar a performance de leitura. Isso envolve deliberadamente permitir algumas duplicações para reduzir a complexidade das consultas.

- **Chaves Estrangeiras**: A normalização frequentemente envolve a criação de chaves estrangeiras para manter a integridade referencial entre tabelas.

#### Exemplo Prático Completo

Vamos considerar um exemplo de um banco de dados para uma livraria. Inicialmente, temos uma tabela não normalizada que armazena informações sobre livros, autores e editoras.

**Tabela Não Normalizada:**

```sql
CREATE TABLE Livros (
    livro_id INT PRIMARY KEY,
    titulo VARCHAR(200),
    autor_nome VARCHAR(100),
    autor_nacionalidade VARCHAR(50),
    editora_nome VARCHAR(100),
    editora_endereco VARCHAR(200)
);
```

**Aplicação das Formas Normais:**

1. **Primeira Forma Normal (1NF)**: Eliminar grupos repetitivos.

```sql
CREATE TABLE Livros (
    livro_id INT PRIMARY KEY,
    titulo VARCHAR(200)
);

CREATE TABLE Autores (
    autor_id INT PRIMARY KEY,
    nome VARCHAR(100),
    nacionalidade VARCHAR(50)
);

CREATE TABLE Livros_Autores (
    livro_id INT,
    autor_id INT,
    PRIMARY KEY (livro_id, autor_id),
    FOREIGN KEY (livro_id) REFERENCES Livros(livro_id),
    FOREIGN KEY (autor_id) REFERENCES Autores(autor_id)
);

CREATE TABLE Editoras (
    editora_id INT PRIMARY KEY,
    nome VARCHAR(100),
    endereco VARCHAR(200)
);
```

2. **Segunda Forma Normal (2NF)**: Eliminar dependências parciais.

```sql
-- Nenhuma dependência parcial foi introduzida, pois já segmentamos adequadamente.
```

3. **Terceira Forma Normal (3NF)**: Eliminar dependências transitivas.

```sql
-- Não há dependências transitivas no exemplo dado.
```

**Conclusão**

A normalização de dados é um processo crucial no design de bancos de dados relacionais, garantindo a eliminação de redundâncias e a manutenção da integridade dos dados. As formas normais fornecem um guia sistemático para refinar o design do banco de dados, resultando em uma estrutura mais eficiente e flexível.
