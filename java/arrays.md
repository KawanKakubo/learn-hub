## Arrays (Vetores) em Java

Em Java, arrays são estruturas de dados que armazenam uma coleção de elementos do mesmo tipo. Eles são usados para organizar e manipular conjuntos de dados de maneira eficiente. A seguir, vamos explorar os conceitos básicos, criação, inicialização, manipulação e algumas operações comuns em arrays.

### Conceito Básico

Um array em Java é uma estrutura de dados que contém elementos de um tipo específico em uma sequência ordenada. Cada elemento no array pode ser acessado pelo seu índice, que começa em 0.

### Criação de Arrays

A sintaxe para criar um array em Java envolve declarar o tipo do array, seguido por colchetes `[]`, e então inicializá-lo usando a palavra-chave `new`.

#### Exemplo de Criação e Inicialização de um Array

```java
// Declaração e criação de um array de inteiros
int[] numeros = new int[5];  // Array de inteiros com 5 elementos

// Inicialização dos elementos do array
numeros[0] = 10;
numeros[1] = 20;
numeros[2] = 30;
numeros[3] = 40;
numeros[4] = 50;
```

#### Inicialização de Array com Valores Padrão

```java
// Criação e inicialização de um array em uma única linha
int[] numeros = {10, 20, 30, 40, 50};
```

### Acessando Elementos de um Array

Os elementos de um array podem ser acessados usando seus índices.

```java
int primeiroElemento = numeros[0];  // Acessa o primeiro elemento do array
int terceiroElemento = numeros[2];  // Acessa o terceiro elemento do array
```

### Iteração sobre Arrays

A maneira mais comum de iterar sobre os elementos de um array é usar um loop `for`.

#### Usando Loop `for` Tradicional

```java
for (int i = 0; i < numeros.length; i++) {
    System.out.println("Elemento no índice " + i + ": " + numeros[i]);
}
```

#### Usando Loop `for-each`

```java
for (int numero : numeros) {
    System.out.println("Número: " + numero);
}
```

### Arrays Multidimensionais

Java suporta arrays multidimensionais, que são arrays de arrays.

#### Criação e Inicialização de Arrays Multidimensionais

```java
// Declaração e criação de um array 2D (matriz) com 3 linhas e 3 colunas
int[][] matriz = new int[3][3];

// Inicialização dos elementos do array 2D
matriz[0][0] = 1;
matriz[0][1] = 2;
matriz[0][2] = 3;
matriz[1][0] = 4;
matriz[1][1] = 5;
matriz[1][2] = 6;
matriz[2][0] = 7;
matriz[2][1] = 8;
matriz[2][2] = 9;
```

#### Inicialização de Arrays Multidimensionais com Valores Padrão

```java
// Criação e inicialização de um array 2D em uma única linha
int[][] matriz = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};
```

#### Iteração sobre Arrays Multidimensionais

```java
for (int i = 0; i < matriz.length; i++) {
    for (int j = 0; j < matriz[i].length; j++) {
        System.out.println("Elemento na posição [" + i + "][" + j + "]: " + matriz[i][j]);
    }
}
```

### Operações Comuns em Arrays

#### Encontrar o Maior e o Menor Elemento

```java
int[] numeros = {10, 20, 30, 40, 50};
int maior = numeros[0];
int menor = numeros[0];

for (int numero : numeros) {
    if (numero > maior) {
        maior = numero;
    }
    if (numero < menor) {
        menor = numero;
    }
}

System.out.println("Maior número: " + maior);
System.out.println("Menor número: " + menor);
```

#### Somar os Elementos de um Array

```java
int soma = 0;

for (int numero : numeros) {
    soma += numero;
}

System.out.println("Soma dos números: " + soma);
```

#### Reverter um Array

```java
int[] numeros = {10, 20, 30, 40, 50};
int[] invertido = new int[numeros.length];

for (int i = 0; i < numeros.length; i++) {
    invertido[i] = numeros[numeros.length - 1 - i];
}

System.out.println("Array invertido: " + Arrays.toString(invertido));
```

### Arrays com Tipos de Dados Não Primitivos

Arrays também podem conter objetos.

#### Exemplo com Strings

```java
String[] nomes = {"Ana", "Carlos", "Maria"};

// Iterando sobre o array de Strings
for (String nome : nomes) {
    System.out.println("Nome: " + nome);
}
```

### Arrays e a Classe `Arrays`

A classe `java.util.Arrays` fornece métodos utilitários para manipular arrays, como classificação e pesquisa.

#### Classificando um Array

```java
int[] numeros = {40, 10, 30, 20, 50};
Arrays.sort(numeros);
System.out.println("Array ordenado: " + Arrays.toString(numeros));
```

#### Pesquisando em um Array

```java
int indice = Arrays.binarySearch(numeros, 30);
System.out.println("Índice do número 30: " + indice);
```

### Conclusão

Os arrays são fundamentais em Java para armazenar e manipular coleções de dados. Eles são simples de usar, mas poderosos o suficiente para muitas aplicações. Com a compreensão dos conceitos básicos e dos métodos utilitários oferecidos pela classe `Arrays`, você pode realizar diversas operações eficientes e úteis com arrays em Java.
