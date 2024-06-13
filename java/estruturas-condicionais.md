## Estruturas Condicionais em Java

As estruturas condicionais em Java permitem que o programa tome decisões e execute blocos específicos de código com base em certas condições. As principais estruturas condicionais em Java são `if`, `if-else`, `if-else if-else`, e `switch`. Vamos explorar cada uma delas com exemplos.

### Estrutura `if`

A estrutura `if` avalia uma condição booleana. Se a condição for verdadeira, o bloco de código associado será executado.

```java
int x = 10;

if (x > 5) {
    System.out.println("x é maior que 5");
}
```

### Estrutura `if-else`

A estrutura `if-else` permite definir um bloco alternativo de código que será executado se a condição for falsa.

```java
int x = 10;

if (x > 15) {
    System.out.println("x é maior que 15");
} else {
    System.out.println("x não é maior que 15");
}
```

### Estrutura `if-else if-else`

A estrutura `if-else if-else` permite verificar múltiplas condições. O bloco correspondente à primeira condição verdadeira será executado. Se nenhuma das condições for verdadeira, o bloco `else` será executado.

```java
int x = 10;

if (x > 15) {
    System.out.println("x é maior que 15");
} else if (x > 5) {
    System.out.println("x é maior que 5, mas não maior que 15");
} else {
    System.out.println("x não é maior que 5");
}
```

### Estrutura `switch`

A estrutura `switch` é utilizada para selecionar uma das muitas seções de código a serem executadas. Ela é mais limpa e organizada para casos em que você precisa verificar várias condições relacionadas ao mesmo valor.

```java
int day = 3;
String dayName;

switch (day) {
    case 1:
        dayName = "Domingo";
        break;
    case 2:
        dayName = "Segunda-feira";
        break;
    case 3:
        dayName = "Terça-feira";
        break;
    case 4:
        dayName = "Quarta-feira";
        break;
    case 5:
        dayName = "Quinta-feira";
        break;
    case 6:
        dayName = "Sexta-feira";
        break;
    case 7:
        dayName = "Sábado";
        break;
    default:
        dayName = "Dia inválido";
        break;
}

System.out.println(dayName);  // Saída: Terça-feira
```

### Operador Ternário

O operador ternário (`?:`) é uma forma concisa de escrever uma expressão `if-else`. Ele avalia uma expressão booleana e retorna um dos dois valores dependendo do resultado da avaliação.

```java
int x = 10;
String resultado = (x > 5) ? "x é maior que 5" : "x não é maior que 5";
System.out.println(resultado);  // Saída: x é maior que 5
```

### Exemplos Práticos

#### Verificação de Paridade

Verificar se um número é par ou ímpar usando `if-else`.

```java
int num = 8;

if (num % 2 == 0) {
    System.out.println(num + " é par");
} else {
    System.out.println(num + " é ímpar");
}
```

#### Classificação de Idade

Classificar a idade de uma pessoa em categorias usando `if-else if-else`.

```java
int idade = 20;

if (idade < 13) {
    System.out.println("Criança");
} else if (idade >= 13 && idade < 18) {
    System.out.println("Adolescente");
} else if (idade >= 18 && idade < 65) {
    System.out.println("Adulto");
} else {
    System.out.println("Idoso");
}
```

#### Dias da Semana com `switch`

Exibir o nome do dia da semana com base em um valor inteiro.

```java
int dia = 5;

switch (dia) {
    case 1:
        System.out.println("Domingo");
        break;
    case 2:
        System.out.println("Segunda-feira");
        break;
    case 3:
        System.out.println("Terça-feira");
        break;
    case 4:
        System.out.println("Quarta-feira");
        break;
    case 5:
        System.out.println("Quinta-feira");
        break;
    case 6:
        System.out.println("Sexta-feira");
        break;
    case 7:
        System.out.println("Sábado");
        break;
    default:
        System.out.println("Dia inválido");
        break;
}
```

### Conclusão

As estruturas condicionais em Java são fundamentais para controlar o fluxo do programa com base em diferentes condições. Com `if`, `if-else`, `if-else if-else`, `switch` e o operador ternário, você pode construir lógica complexa e tomar decisões dentro de seu código de forma clara e eficiente. Essas estruturas são essenciais para a programação e ajudam a tornar seus programas mais dinâmicos e responsivos.
