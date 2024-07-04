### Criação de Tabelas em MySQL

Para criar uma tabela em MySQL, usa-se o comando `CREATE TABLE`. Aqui está um exemplo básico:

```sql
CREATE TABLE alunos (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(100),
    idade INT,
    data_nascimento DATE
);
```

### Atualização de Valores

Para atualizar valores em uma tabela, usa-se o comando `UPDATE`. Você pode atualizar um ou mais campos com base em uma condição (`WHERE`).

```sql
UPDATE alunos
SET idade = 21
WHERE id = 1;
```

### Deletando Tabelas

Para deletar uma tabela, usa-se o comando `DROP TABLE`.

```sql
DROP TABLE alunos;
```

### Copiando Tudo de uma Tabela

Para copiar todos os dados de uma tabela para outra, primeiro crie a nova tabela com a mesma estrutura (ou diferente, conforme necessário), e depois use o comando `INSERT INTO ... SELECT`.

#### Criando uma nova tabela com a mesma estrutura:

```sql
CREATE TABLE alunos_backup LIKE alunos;
```

#### Copiando os dados:

```sql
INSERT INTO alunos_backup
SELECT * FROM alunos;
```

### Adicionar Linhas

Para adicionar uma única linha, usa-se o comando `INSERT INTO`.

```sql
INSERT INTO alunos (nome, idade, data_nascimento)
VALUES ('Maria Silva', 20, '2002-05-15');
```

### Adicionar Múltiplas Linhas

Para adicionar múltiplas linhas de uma vez, também usa-se o comando `INSERT INTO`, mas com várias tuplas de valores.

```sql
INSERT INTO alunos (nome, idade, data_nascimento)
VALUES 
('João Souza', 22, '2000-03-10'),
('Ana Costa', 19, '2003-08-21'),
('Carlos Lima', 21, '2001-01-30');
```

### Atualizando Múltiplas Linhas

Você pode atualizar múltiplas linhas com base em uma condição usando o comando `UPDATE`.

```sql
UPDATE alunos
SET idade = idade + 1
WHERE data_nascimento < '2000-01-01';
```

### Deletando Linhas

Para deletar linhas específicas de uma tabela, usa-se o comando `DELETE`.

```sql
DELETE FROM alunos
WHERE idade > 25;
```

### Exemplos Completos

#### Criando uma Tabela
```sql
CREATE TABLE funcionarios (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(100),
    cargo VARCHAR(50),
    salario DECIMAL(10, 2),
    data_admissao DATE
);
```

#### Adicionando Linhas
```sql
INSERT INTO funcionarios (nome, cargo, salario, data_admissao)
VALUES 
('Pedro Santos', 'Gerente', 5000.00, '2018-02-15'),
('Luciana Alves', 'Analista', 3000.00, '2019-05-10');
```

#### Atualizando Valores
```sql
UPDATE funcionarios
SET salario = salario * 1.1
WHERE cargo = 'Analista';
```

#### Deletando Linhas
```sql
DELETE FROM funcionarios
WHERE cargo = 'Gerente';
```

#### Copiando Tabela
```sql
CREATE TABLE funcionarios_backup LIKE funcionarios;

INSERT INTO funcionarios_backup
SELECT * FROM funcionarios;
```

Com esses comandos, você consegue gerenciar tabelas e dados no MySQL de maneira eficaz.
