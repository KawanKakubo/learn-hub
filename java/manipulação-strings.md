## Manipulação de Strings em Java

### Strings

Em Java, uma `String` é um objeto que representa uma sequência de caracteres. A classe `String` oferece muitos métodos para manipular strings.

### Criação de Strings

```java
String str1 = "Olá, Mundo!";
String str2 = new String("Olá, Mundo!");
```

### Principais Métodos de `String`

#### `length()`

Retorna o comprimento da string.

```java
int length = str1.length();  // Saída: 12
```

#### `charAt()`

Retorna o caractere em uma posição específica.

```java
char ch = str1.charAt(1);  // Saída: 'l'
```

#### `substring()`

Retorna uma parte da string.

```java
String sub = str1.substring(4, 9);  // Saída: ", Mun"
```

#### `equals()`

Compara duas strings para igualdade.

```java
boolean isEqual = str1.equals(str2);  // Saída: true
```

#### `equalsIgnoreCase()`

Compara duas strings para igualdade, ignorando diferenças de maiúsculas e minúsculas.

```java
boolean isEqualIgnoreCase = str1.equalsIgnoreCase("olá, mundo!");  // Saída: true
```

#### `indexOf()`

Retorna o índice da primeira ocorrência de um caractere ou substring.

```java
int index = str1.indexOf('M');  // Saída: 5
```

#### `toUpperCase()`

Converte todos os caracteres da string para maiúsculas.

```java
String upper = str1.toUpperCase();  // Saída: "OLÁ, MUNDO!"
```

#### `toLowerCase()`

Converte todos os caracteres da string para minúsculas.

```java
String lower = str1.toLowerCase();  // Saída: "olá, mundo!"
```

#### `trim()`

Remove espaços em branco do início e do fim da string.

```java
String trimmed = "   Espaços   ".trim();  // Saída: "Espaços"
```

#### `replace()`

Substitui todas as ocorrências de um caractere ou substring por outro.

```java
String replaced = str1.replace("Mundo", "Java");  // Saída: "Olá, Java!"
```

### StringBuilder e StringBuffer

`StringBuilder` e `StringBuffer` são usadas para manipulação eficiente de strings mutáveis.

#### `StringBuilder`

```java
StringBuilder sb = new StringBuilder("Olá");
sb.append(", Mundo!");
String result = sb.toString();  // Saída: "Olá, Mundo!"
```

#### `StringBuffer`

`StringBuffer` é semelhante a `StringBuilder`, mas é sincronizado e seguro para threads.

```java
StringBuffer sbf = new StringBuffer("Olá");
sbf.append(", Mundo!");
String result = sbf.toString();  // Saída: "Olá, Mundo!"
```

## Manipulação de Datas em Java

### java.util.Date

A classe `Date` representa uma data e hora específica.

#### Criação de um objeto `Date`

```java
Date date = new Date();
System.out.println(date);
```

### java.text.SimpleDateFormat

A classe `SimpleDateFormat` é usada para formatação e análise de datas.

#### Formatação de Datas

```java
SimpleDateFormat sdf = new SimpleDateFormat("dd/MM/yyyy HH:mm:ss");
String formattedDate = sdf.format(date);  // Exemplo de saída: "04/06/2024 14:35:10"
```

#### Análise de Datas

```java
String dateStr = "04/06/2024 14:35:10";
Date parsedDate = sdf.parse(dateStr);
```

### java.time (Java 8+)

A API de data e hora introduzida no Java 8 (`java.time`) é mais robusta e oferece diversas classes para trabalhar com datas e horas.

#### LocalDate

Representa uma data (ano, mês, dia) sem hora.

```java
LocalDate today = LocalDate.now();
LocalDate birthday = LocalDate.of(1990, Month.JUNE, 4);
```

#### LocalTime

Representa uma hora do dia sem data.

```java
LocalTime now = LocalTime.now();
LocalTime specificTime = LocalTime.of(14, 30, 0);
```

#### LocalDateTime

Combina uma data e uma hora.

```java
LocalDateTime currentDateTime = LocalDateTime.now();
LocalDateTime meeting = LocalDateTime.of(2024, Month.JUNE, 4, 14, 30);
```

#### DateTimeFormatter

Formatar e analisar datas e horas com a API `java.time`.

```java
DateTimeFormatter formatter = DateTimeFormatter.ofPattern("dd/MM/yyyy HH:mm:ss");
String formattedDateTime = currentDateTime.format(formatter);  // Saída: "04/06/2024 14:35:10"

String dateTimeStr = "04/06/2024 14:35:10";
LocalDateTime parsedDateTime = LocalDateTime.parse(dateTimeStr, formatter);
```

### Comparação de Datas

#### Comparando LocalDate

```java
LocalDate date1 = LocalDate.of(2024, 6, 4);
LocalDate date2 = LocalDate.of(2023, 12, 25);

boolean isBefore = date1.isBefore(date2);  // false
boolean isAfter = date1.isAfter(date2);    // true
```

#### Comparando Date (java.util.Date)

```java
Date date1 = new Date();
Date date2 = new Date(System.currentTimeMillis() - 1000 * 60 * 60 * 24);  // Um dia antes

boolean isBefore = date1.before(date2);  // false
boolean isAfter = date1.after(date2);    // true
```

## Conclusão

A manipulação de strings e datas é uma parte fundamental do desenvolvimento em Java. A classe `String` fornece métodos robustos para manipulação de textos, enquanto `StringBuilder` e `StringBuffer` são utilizados para operações mais eficientes e seguras com strings mutáveis. Para manipulação de datas, Java oferece tanto as classes mais antigas como `Date` e `SimpleDateFormat`, quanto a moderna e poderosa API `java.time` introduzida no Java 8, que torna o trabalho com datas e horas mais intuitivo e menos propenso a erros.
