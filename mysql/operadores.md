### Tipos de Operadores em MySQL

MySQL suporta vários tipos de operadores que são usados em expressões para realizar operações em dados. Aqui estão os principais tipos de operadores disponíveis em MySQL:

#### Operadores Aritméticos
Esses operadores são usados para realizar operações aritméticas em valores numéricos.

- `+` (Adição): Adiciona dois valores.
- `-` (Subtração): Subtrai o segundo valor do primeiro.
- `*` (Multiplicação): Multiplica dois valores.
- `/` (Divisão): Divide o primeiro valor pelo segundo.
- `%` (Módulo): Retorna o restante da divisão do primeiro valor pelo segundo.

```sql
SELECT 10 + 5;    -- Retorna 15
SELECT 10 - 5;    -- Retorna 5
SELECT 10 * 5;    -- Retorna 50
SELECT 10 / 5;    -- Retorna 2
SELECT 10 % 3;    -- Retorna 1
```

#### Operadores de Comparação
Esses operadores são usados para comparar dois valores. O resultado de uma comparação é um valor booleano (`TRUE` ou `FALSE`).

- `=` (Igual a): Compara se dois valores são iguais.
- `!=` ou `<>` (Diferente de): Compara se dois valores são diferentes.
- `>` (Maior que): Compara se o primeiro valor é maior que o segundo.
- `<` (Menor que): Compara se o primeiro valor é menor que o segundo.
- `>=` (Maior ou igual a): Compara se o primeiro valor é maior ou igual ao segundo.
- `<=` (Menor ou igual a): Compara se o primeiro valor é menor ou igual ao segundo.
- `<=>` (Igual nulo-seguro): Compara se dois valores são iguais, incluindo `NULL`.

```sql
SELECT 10 = 5;    -- Retorna FALSE
SELECT 10 != 5;   -- Retorna TRUE
SELECT 10 > 5;    -- Retorna TRUE
SELECT 10 < 5;    -- Retorna FALSE
SELECT 10 >= 5;   -- Retorna TRUE
SELECT 10 <= 5;   -- Retorna FALSE
SELECT 10 <=> NULL; -- Retorna FALSE
SELECT NULL <=> NULL; -- Retorna TRUE
```

#### Operadores Lógicos
Esses operadores são usados para combinar condições lógicas.

- `AND`: Retorna `TRUE` se ambas as condições forem verdadeiras.
- `OR`: Retorna `TRUE` se pelo menos uma das condições for verdadeira.
- `NOT`: Inverte o valor lógico de uma condição.

```sql
SELECT TRUE AND FALSE; -- Retorna FALSE
SELECT TRUE OR FALSE;  -- Retorna TRUE
SELECT NOT TRUE;       -- Retorna FALSE
```

#### Operadores de Bits
Esses operadores realizam operações a nível de bit em valores inteiros.

- `&` (AND bit a bit): Realiza uma operação AND bit a bit.
- `|` (OR bit a bit): Realiza uma operação OR bit a bit.
- `^` (XOR bit a bit): Realiza uma operação XOR bit a bit.
- `~` (NOT bit a bit): Inverte todos os bits.
- `<<` (Deslocamento à esquerda): Desloca os bits para a esquerda.
- `>>` (Deslocamento à direita): Desloca os bits para a direita.

```sql
SELECT 5 & 3;    -- Retorna 1
SELECT 5 | 3;    -- Retorna 7
SELECT 5 ^ 3;    -- Retorna 6
SELECT ~5;       -- Retorna -6
SELECT 5 << 1;   -- Retorna 10
SELECT 5 >> 1;   -- Retorna 2
```

#### Operadores de Atribuição
Esses operadores são usados para atribuir valores a variáveis.

- `:=`: Atribui um valor a uma variável.

```sql
SET @var := 10;
SELECT @var;     -- Retorna 10
```

#### Operadores de Strings
Esses operadores são usados para concatenar strings.

- `CONCAT()`: Concatena duas ou mais strings.
- `||`: Concatena duas ou mais strings (pode depender do modo de compatibilidade SQL).
- `BINARY`: Força uma comparação de strings a ser sensível a maiúsculas e minúsculas.

```sql
SELECT CONCAT('Hello', ' ', 'World'); -- Retorna 'Hello World'
SELECT 'Hello' || ' World';           -- Pode retornar 'Hello World'
SELECT BINARY 'a' = 'A';              -- Retorna FALSE
```

#### Operadores Especiais
- `BETWEEN`: Verifica se um valor está dentro de um intervalo.
- `IN`: Verifica se um valor está dentro de um conjunto de valores.
- `LIKE`: Verifica se um valor de string corresponde a um padrão.
- `IS NULL`: Verifica se um valor é `NULL`.
- `IS NOT NULL`: Verifica se um valor não é `NULL`.

```sql
SELECT 5 BETWEEN 1 AND 10;         -- Retorna TRUE
SELECT 5 IN (1, 2, 3, 4, 5);       -- Retorna TRUE
SELECT 'Hello' LIKE 'H%';          -- Retorna TRUE
SELECT NULL IS NULL;               -- Retorna TRUE
SELECT NULL IS NOT NULL;           -- Retorna FALSE
```

Esses operadores formam a base para realizar diversas operações em consultas SQL no MySQL, permitindo manipulação e consulta eficiente dos dados armazenados no banco de dados.
