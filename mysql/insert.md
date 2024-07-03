Para adicionar uma ou várias linhas em uma tabela no MySQL, você pode usar o comando `INSERT INTO`. Vou fornecer exemplos para ambos os casos.

### Adicionando uma única linha

Para adicionar uma única linha a uma tabela, você pode usar o seguinte comando:

```sql
INSERT INTO nome_da_tabela (coluna1, coluna2, coluna3) 
VALUES (valor1, valor2, valor3);
```

Por exemplo, considerando a tabela `usuarios` criada anteriormente:

```sql
INSERT INTO usuarios (nome, email) 
VALUES ('Maria Souza', 'maria@example.com');
```

### Adicionando várias linhas

Para adicionar várias linhas de uma vez, você pode usar o comando `INSERT INTO` com múltiplos conjuntos de valores:

```sql
INSERT INTO nome_da_tabela (coluna1, coluna2, coluna3) 
VALUES 
(valor1a, valor2a, valor3a),
(valor1b, valor2b, valor3b),
(valor1c, valor2c, valor3c);
```

Novamente, considerando a tabela `usuarios`:

```sql
INSERT INTO usuarios (nome, email) 
VALUES 
('Carlos Pereira', 'carlos@example.com'),
('Ana Oliveira', 'ana@example.com'),
('Roberto Lima', 'roberto@example.com');
```

### Exemplo completo

Vamos revisar um exemplo completo, incluindo a criação da tabela e a inserção de várias linhas:

```sql
-- Criação da tabela
CREATE TABLE usuarios (
    id INT NOT NULL AUTO_INCREMENT,
    nome VARCHAR(100) NOT NULL,
    email VARCHAR(100) NOT NULL,
    PRIMARY KEY (id)
);

-- Inserindo uma única linha
INSERT INTO usuarios (nome, email) 
VALUES ('Maria Souza', 'maria@example.com');

-- Inserindo várias linhas
INSERT INTO usuarios (nome, email) 
VALUES 
('Carlos Pereira', 'carlos@example.com'),
('Ana Oliveira', 'ana@example.com'),
('Roberto Lima', 'roberto@example.com');
```

Este exemplo demonstra como criar uma tabela e adicionar tanto uma única linha quanto múltiplas linhas na tabela `usuarios`.
