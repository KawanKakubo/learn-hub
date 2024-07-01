# Expressões Regulares (RegEx) em Detalhe

As expressões regulares (RegEx) são uma ferramenta poderosa para trabalhar com padrões de texto. Elas permitem procurar, substituir e manipular texto com grande precisão. Vamos explorar os principais conceitos e operadores das expressões regulares com exemplos para ajudar a compreender como usá-las efetivamente.

## Conceitos Básicos

Uma expressão regular é uma sequência de caracteres que define um padrão de pesquisa. Esse padrão pode ser usado para fazer correspondências dentro de uma string. As expressões regulares são amplamente usadas em linguagens de programação e ferramentas de texto para validação, pesquisa, e substituição de padrões.

## Principais Operadores de RegEx

### 1. `.` (Ponto)
Corresponde a qualquer caractere, exceto uma nova linha.

#### Exemplo:
- `a.b` corresponderá a "aab", "acb", "a1b", etc.

### 2. `^` (Circunflexo)
Corresponde ao início de uma linha ou string.

#### Exemplo:
- `^Hello` corresponderá a qualquer string que comece com "Hello".

### 3. `$` (Cifrão)
Corresponde ao fim de uma linha ou string.

#### Exemplo:
- `world$` corresponderá a qualquer string que termine com "world".

### 4. `*` (Asterisco)
Corresponde a zero ou mais ocorrências do elemento que o precede.

#### Exemplo:
- `ab*c` corresponderá a "ac", "abc", "abbc", etc.

### 5. `+` (Mais)
Corresponde a uma ou mais ocorrências do elemento que o precede.

#### Exemplo:
- `ab+c` corresponderá a "abc", "abbc", "abbbc", etc., mas não "ac".

### 6. `?` (Interrogação)
Corresponde a zero ou uma ocorrência do elemento que o precede.

#### Exemplo:
- `colou?r` corresponderá a "color" e "colour".

### 7. `{n}`
Corresponde exatamente a `n` ocorrências do elemento que o precede.

#### Exemplo:
- `a{3}` corresponderá a "aaa".

### 8. `{n,}`
Corresponde a `n` ou mais ocorrências do elemento que o precede.

#### Exemplo:
- `a{2,}` corresponderá a "aa", "aaa", "aaaa", etc.

### 9. `{n,m}`
Corresponde a pelo menos `n` e no máximo `m` ocorrências do elemento que o precede.

#### Exemplo:
- `a{2,4}` corresponderá a "aa", "aaa", "aaaa".

### 10. `[]` (Colchetes)
Define um conjunto de caracteres, correspondendo a qualquer caractere dentro dos colchetes.

#### Exemplo:
- `[abc]` corresponderá a "a", "b", ou "c".

### 11. `|` (Barra Vertical)
Corresponde a uma alternativa entre dois padrões.

#### Exemplo:
- `cat|dog` corresponderá a "cat" ou "dog".

### 12. `\` (Barra Invertida)
Escapa caracteres especiais para tratá-los como literais ou introduz metacaracteres específicos.

#### Exemplo:
- `\d` corresponde a qualquer dígito. Equivalente a `[0-9]`.

## Agrupamento e Captura

### 1. `()` (Parênteses)
Usados para agrupar partes de uma expressão regular, permitindo aplicar operadores a grupos de caracteres.

#### Exemplo:
- `(ab)+` corresponderá a "ab", "abab", "ababab", etc.

### 2. `(?:...)` (Non-capturing group)
Agrupa caracteres sem capturá-los para referenciamento posterior.

#### Exemplo:
- `(?:ab)+` corresponderá a "ab", "abab", "ababab", etc., mas sem capturar os grupos.

## Uso Comum em MySQL

### `REGEXP`
No MySQL, o operador `REGEXP` permite buscar padrões dentro de strings usando expressões regulares.

#### Exemplos:
1. Verificar endereços de email que podem ter ".com" ou ".co":
   ```sql
   SELECT * FROM usuarios WHERE email REGEXP '\\.co(m)?$';
   ```

2. Encontrar strings que terminam com "ing":
   ```sql
   SELECT * FROM atividades WHERE descricao REGEXP 'ing$';
   ```

3. Verificar telefones que podem ter código de área opcional:
   ```sql
   SELECT * FROM contatos WHERE telefone REGEXP '^(\d{2})? ?\d{4,5}-\d{4}$';
   ```

## Operadores Avançados

### 1. `\b` e `\B`
- `\b` corresponde a uma borda de palavra.
- `\B` corresponde a uma não-borda de palavra.

#### Exemplos:
- `\bword\b` corresponderá a "word" como uma palavra completa.
- `\Bword\B` corresponderá a "word" dentro de outras palavras, como "swordfish".

### 2. `\w`, `\W`, `\d`, `\D`, `\s`, `\S`
- `\w` corresponde a qualquer caractere alfanumérico.
- `\W` corresponde a qualquer caractere não alfanumérico.
- `\d` corresponde a qualquer dígito.
- `\D` corresponde a qualquer caractere não dígito.
- `\s` corresponde a qualquer espaço em branco.
- `\S` corresponde a qualquer caractere não espaço em branco.

### 3. Ancoragens
- `^` ancoragem ao início da string.
- `$` ancoragem ao fim da string.

## Exemplos Comuns de RegEx no Dia a Dia

1. **Validar endereços de email:**
   ```regex
   ^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$
   ```

2. **Validar números de telefone:**
   ```regex
   ^\(?\d{3}\)?[-.\s]?\d{3}[-.\s]?\d{4}$
   ```

3. **Validar URLs:**
   ```regex
   ^(http|https):\/\/[^\s$.?#].[^\s]*$
   ```

4. **Validar código postal (CEP) brasileiro:**
   ```regex
   ^\d{5}-\d{3}$
   ```

## Conclusão

As expressões regulares são ferramentas essenciais para trabalhar com texto em programação. Entender os operadores básicos e avançados permite criar padrões precisos para validação, pesquisa e manipulação de strings. Praticar com exemplos reais e usar as expressões regulares em diferentes contextos ajudará a dominar esta poderosa ferramenta.
