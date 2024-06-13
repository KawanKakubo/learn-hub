## Variáveis e Tipos Primitivos de Dados em Java

Java é uma linguagem de programação fortemente tipada e orientada a objetos. Uma parte fundamental da programação em Java é entender como declarar, inicializar e utilizar variáveis, bem como os tipos primitivos de dados que a linguagem suporta.

### Variáveis em Java

Variáveis são contêineres usados para armazenar dados que podem ser utilizados e manipulados em um programa. Em Java, todas as variáveis precisam ser declaradas antes de serem usadas. A declaração de uma variável inclui o tipo de dado que ela pode armazenar e o nome da variável.

#### Declaração de Variáveis

A sintaxe básica para declarar uma variável em Java é:

```java
tipo nomeDaVariavel;
```

Exemplo:

```java
int idade;
double salario;
char inicial;
```

#### Inicialização de Variáveis

A inicialização de variáveis pode ocorrer no momento da declaração ou posteriormente. Inicializar uma variável significa atribuir um valor inicial a ela.

Exemplo:

```java
int idade = 25;
double salario = 55000.75;
char inicial = 'J';
```

#### Tipos de Variáveis

Existem três tipos principais de variáveis em Java:

1. **Variáveis de Instância (não estáticas)**: Atributos de uma classe que são criados quando um objeto é instanciado e são destruídos quando o objeto é destruído.
2. **Variáveis de Classe (estáticas)**: Atributos que são compartilhados entre todas as instâncias de uma classe. São declaradas usando a palavra-chave `static`.
3. **Variáveis Locais**: Declaradas dentro de métodos, construtores ou blocos. São criadas quando o bloco é iniciado e destruídas quando o bloco é encerrado.

### Tipos Primitivos de Dados em Java

Java suporta oito tipos primitivos de dados, que são os blocos de construção fundamentais para a manipulação de dados. Eles são predefinidos pela linguagem e não são objetos.

#### Tipos Numéricos Inteiros

1. **byte**
   - Tamanho: 8 bits
   - Intervalo: -128 a 127
   - Exemplo:
     ```java
     byte idade = 30;
     ```

2. **short**
   - Tamanho: 16 bits
   - Intervalo: -32.768 a 32.767
   - Exemplo:
     ```java
     short temperatura = 100;
     ```

3. **int**
   - Tamanho: 32 bits
   - Intervalo: -2^31 a 2^31 - 1
   - Exemplo:
     ```java
     int populacao = 1000000;
     ```

4. **long**
   - Tamanho: 64 bits
   - Intervalo: -2^63 a 2^63 - 1
   - Exemplo:
     ```java
     long distancia = 15000000000L;  // Nota: o sufixo 'L' indica um valor long
     ```

#### Tipos Numéricos de Ponto Flutuante

1. **float**
   - Tamanho: 32 bits
   - Intervalo: aproximadamente ±3.40282347E+38F (6-7 dígitos decimais significativos)
   - Exemplo:
     ```java
     float preco = 19.99F;  // Nota: o sufixo 'F' indica um valor float
     ```

2. **double**
   - Tamanho: 64 bits
   - Intervalo: aproximadamente ±1.79769313486231570E+308 (15 dígitos decimais significativos)
   - Exemplo:
     ```java
     double salario = 55000.75;
     ```

#### Tipo Caractere

1. **char**
   - Tamanho: 16 bits
   - Intervalo: 0 a 65.535 (valores unicode)
   - Exemplo:
     ```java
     char inicial = 'A';
     ```

#### Tipo Booleano

1. **boolean**
   - Tamanho: 1 bit
   - Valores: `true` ou `false`
   - Exemplo:
     ```java
     boolean isAtivo = true;
     ```

### Conversão de Tipos

Em Java, é possível converter tipos de dados de um tipo para outro. A conversão pode ser implícita (automática) ou explícita (manual).

#### Conversão Implícita (Widening)

Quando o tipo de destino é maior que o tipo de origem, a conversão é feita automaticamente.

Exemplo:

```java
int num = 100;
long bigNum = num;  // Conversão implícita de int para long
```

#### Conversão Explícita (Narrowing)

Quando o tipo de destino é menor que o tipo de origem, a conversão deve ser feita explicitamente.

Exemplo:

```java
long bigNum = 100000L;
int num = (int) bigNum;  // Conversão explícita de long para int
```

### Variáveis Final

Em Java, a palavra-chave `final` é usada para declarar constantes. Uma variável final não pode ter seu valor alterado após a inicialização.

Exemplo:

```java
final double PI = 3.14159;
```

### Conclusão

Entender variáveis e tipos primitivos de dados é essencial para qualquer programador Java. Esses conceitos formam a base sobre a qual programas mais complexos são construídos. Variáveis permitem armazenar e manipular dados, enquanto os tipos primitivos fornecem os tipos básicos de dados que podem ser utilizados.
