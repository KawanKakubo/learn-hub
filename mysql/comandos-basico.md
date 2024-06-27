### Comandos SQL em MySQL

#### USE
O comando `USE` é utilizado para selecionar um banco de dados específico com o qual você deseja trabalhar. Após selecionar um banco de dados, todas as operações subsequentes serão realizadas nesse banco.

```sql
USE nome_do_banco_de_dados;
```

#### SELECT
O comando `SELECT` é utilizado para consultar dados de um banco de dados. Você pode selecionar todas as colunas de uma tabela ou apenas algumas específicas.

```sql
-- Selecionando todas as colunas de uma tabela
SELECT * FROM nome_da_tabela;

-- Selecionando colunas específicas
SELECT coluna1, coluna2 FROM nome_da_tabela;
```

#### FROM
O comando `FROM` é usado junto com o `SELECT` para especificar a tabela da qual os dados serão extraídos.

```sql
SELECT coluna1, coluna2 FROM nome_da_tabela;
```

#### WHERE
O comando `WHERE` é utilizado para filtrar registros que atendem a uma condição específica. Somente os registros que satisfazem a condição serão incluídos no resultado.

```sql
SELECT coluna1, coluna2 
FROM nome_da_tabela 
WHERE condição;
```

**Exemplos:**

```sql
-- Selecionando registros onde a idade é maior que 25
SELECT nome, idade 
FROM clientes 
WHERE idade > 25;

-- Selecionando registros onde o nome é 'João'
SELECT nome, idade 
FROM clientes 
WHERE nome = 'João';
```

#### ORDER BY
O comando `ORDER BY` é utilizado para ordenar os resultados de uma consulta. Por padrão, a ordenação é feita em ordem crescente (ASC). Para ordenar em ordem decrescente, utiliza-se a palavra-chave `DESC`.

```sql
SELECT coluna1, coluna2 
FROM nome_da_tabela 
ORDER BY coluna1 ASC;  -- Ordem crescente

SELECT coluna1, coluna2 
FROM nome_da_tabela 
ORDER BY coluna1 DESC; -- Ordem decrescente
```

**Exemplo:**

```sql
-- Selecionando todos os clientes e ordenando pelo nome em ordem crescente
SELECT nome, idade 
FROM clientes 
ORDER BY nome ASC;

-- Selecionando todos os clientes e ordenando pela idade em ordem decrescente
SELECT nome, idade 
FROM clientes 
ORDER BY idade DESC;
```

#### Exemplo Completo
Vamos combinar os comandos acima em uma consulta completa:

```sql
-- Usar o banco de dados `meu_banco`
USE meu_banco;

-- Selecionar os nomes e idades dos clientes onde a idade é maior que 25 e ordenar pelo nome
SELECT nome, idade 
FROM clientes 
WHERE idade > 25 
ORDER BY nome ASC;
```

**Descrição:**

1. **USE meu_banco**: Seleciona o banco de dados `meu_banco`.
2. **SELECT nome, idade FROM clientes**: Seleciona as colunas `nome` e `idade` da tabela `clientes`.
3. **WHERE idade > 25**: Filtra os registros para incluir apenas aqueles onde a idade é maior que 25.
4. **ORDER BY nome ASC**: Ordena os resultados pelo nome em ordem crescente.

Esses comandos básicos permitem realizar operações fundamentais para consultar e manipular dados em um banco de dados MySQL.
