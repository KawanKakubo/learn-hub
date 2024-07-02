### INNER JOIN e Filtros com JOIN em MySQL

O `INNER JOIN` é uma das operações mais comuns em SQL para combinar registros de duas ou mais tabelas. Ele retorna apenas os registros que possuem valores correspondentes em ambas as tabelas envolvidas na junção. Vamos explorar como usar `INNER JOIN` e aplicar filtros ao mesmo tempo.

#### Sintaxe Básica do INNER JOIN
```sql
SELECT colunas
FROM tabela1
INNER JOIN tabela2
ON tabela1.coluna_comum = tabela2.coluna_comum;
```

#### Exemplo Prático
Considere duas tabelas, `clientes` e `pedidos`, onde queremos listar os clientes que têm pedidos associados.

```sql
SELECT clientes.nome, pedidos.data_pedido
FROM clientes
INNER JOIN pedidos
ON clientes.id = pedidos.cliente_id;
```
Neste exemplo, a consulta retorna apenas os clientes que têm registros na tabela `pedidos`.

### Filtros com JOIN

Para filtrar os resultados de um `INNER JOIN`, você pode usar a cláusula `WHERE`. A combinação de `INNER JOIN` e `WHERE` permite que você refine os resultados com base em condições adicionais.

#### Sintaxe Básica com Filtros
```sql
SELECT colunas
FROM tabela1
INNER JOIN tabela2
ON tabela1.coluna_comum = tabela2.coluna_comum
WHERE condições;
```

#### Exemplo Prático com Filtros
Vamos estender o exemplo anterior para incluir um filtro que retorna apenas pedidos realizados após uma determinada data.

```sql
SELECT clientes.nome, pedidos.data_pedido
FROM clientes
INNER JOIN pedidos
ON clientes.id = pedidos.cliente_id
WHERE pedidos.data_pedido > '2023-01-01';
```
Esta consulta retorna apenas os clientes que fizeram pedidos após 1 de janeiro de 2023.

### Consultas com Várias Tabelas

Você pode usar múltiplos `INNER JOIN` para juntar mais de duas tabelas em uma única consulta.

#### Exemplo Prático com Várias Tabelas
Considere três tabelas: `clientes`, `pedidos` e `produtos`. Queremos listar os nomes dos clientes, as datas dos pedidos e os nomes dos produtos pedidos.

```sql
SELECT clientes.nome AS nome_cliente, pedidos.data_pedido, produtos.nome AS nome_produto
FROM clientes
INNER JOIN pedidos
ON clientes.id = pedidos.cliente_id
INNER JOIN produtos
ON pedidos.produto_id = produtos.id;
```
Este exemplo retorna uma lista de clientes com as datas dos pedidos e os nomes dos produtos pedidos.

### Uso de Alias para Simplificação

O uso de alias pode simplificar a leitura e a escrita das consultas, especialmente quando se trabalha com múltiplas tabelas.

#### Exemplo com Alias
```sql
SELECT c.nome AS nome_cliente, p.data_pedido, pr.nome AS nome_produto
FROM clientes AS c
INNER JOIN pedidos AS p
ON c.id = p.cliente_id
INNER JOIN produtos AS pr
ON p.produto_id = pr.id;
```
Os alias `c`, `p` e `pr` tornam a consulta mais legível.

### Filtros com JOIN em Múltiplas Tabelas

Quando você combina várias tabelas, pode aplicar filtros que envolvam qualquer uma das tabelas envolvidas.

#### Exemplo de Filtros com Múltiplas Tabelas
Vamos adicionar um filtro que seleciona apenas os pedidos de um determinado produto.

```sql
SELECT c.nome AS nome_cliente, p.data_pedido, pr.nome AS nome_produto
FROM clientes AS c
INNER JOIN pedidos AS p
ON c.id = p.cliente_id
INNER JOIN produtos AS pr
ON p.produto_id = pr.id
WHERE pr.nome = 'Produto X';
```
Este exemplo retorna apenas os clientes que fizeram pedidos do "Produto X".

### Conclusão

Usar `INNER JOIN` para combinar tabelas e aplicar filtros com `WHERE` é uma técnica poderosa para extrair dados específicos de um banco de dados relacional. Com a prática, você poderá escrever consultas complexas que envolvem múltiplas tabelas e condições de filtro, facilitando a análise e a manipulação de grandes conjuntos de dados.
