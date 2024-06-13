## Operadores em Java

Os operadores são símbolos que instruem o compilador a realizar operações específicas em uma ou mais operandos. Java oferece uma ampla gama de operadores, incluindo aritméticos, relacionais, lógicos, bit a bit, de atribuição e ternários.

### Operadores Aritméticos

Os operadores aritméticos são usados para realizar operações matemáticas comuns.

- **Adição** (`+`): Soma dois operandos.
  ```java
  int a = 10;
  int b = 5;
  int resultado = a + b;  // resultado = 15
  ```

- **Subtração** (`-`): Subtrai o segundo operando do primeiro.
  ```java
  int resultado = a - b;  // resultado = 5
  ```

- **Multiplicação** (`*`): Multiplica dois operandos.
  ```java
  int resultado = a * b;  // resultado = 50
  ```

- **Divisão** (`/`): Divide o primeiro operando pelo segundo. Se ambos os operandos forem inteiros, a divisão será inteira.
  ```java
  int resultado = a / b;  // resultado = 2
  ```

- **Módulo** (`%`): Retorna o resto da divisão do primeiro operando pelo segundo.
  ```java
  int resultado = a % b;  // resultado = 0
  ```

### Operadores Relacionais

Os operadores relacionais comparam dois operandos e retornam um valor booleano (`true` ou `false`).

- **Igual a** (`==`): Verifica se dois operandos são iguais.
  ```java
  boolean resultado = (a == b);  // resultado = false
  ```

- **Diferente de** (`!=`): Verifica se dois operandos são diferentes.
  ```java
  boolean resultado = (a != b);  // resultado = true
  ```

- **Maior que** (`>`): Verifica se o primeiro operando é maior que o segundo.
  ```java
  boolean resultado = (a > b);  // resultado = true
  ```

- **Menor que** (`<`): Verifica se o primeiro operando é menor que o segundo.
  ```java
  boolean resultado = (a < b);  // resultado = false
  ```

- **Maior ou igual a** (`>=`): Verifica se o primeiro operando é maior ou igual ao segundo.
  ```java
  boolean resultado = (a >= b);  // resultado = true
  ```

- **Menor ou igual a** (`<=`): Verifica se o primeiro operando é menor ou igual ao segundo.
  ```java
  boolean resultado = (a <= b);  // resultado = false
  ```

### Operadores Lógicos

Os operadores lógicos são usados para combinar duas ou mais condições booleanas.

- **E lógico** (`&&`): Retorna `true` se ambas as condições forem verdadeiras.
  ```java
  boolean resultado = (a > 0 && b > 0);  // resultado = true
  ```

- **Ou lógico** (`||`): Retorna `true` se pelo menos uma das condições for verdadeira.
  ```java
  boolean resultado = (a > 0 || b < 0);  // resultado = true
  ```

- **Não lógico** (`!`): Inverte o valor da condição.
  ```java
  boolean resultado = !(a > 0);  // resultado = false
  ```

### Operadores de Atribuição

Os operadores de atribuição são usados para atribuir valores a variáveis.

- **Atribuição simples** (`=`): Atribui o valor do operando direito ao operando esquerdo.
  ```java
  int c = a;
  ```

- **Atribuição aditiva** (`+=`): Adiciona o valor do operando direito ao operando esquerdo e atribui o resultado ao operando esquerdo.
  ```java
  a += b;  // Equivalente a a = a + b;
  ```

- **Atribuição subtrativa** (`-=`): Subtrai o valor do operando direito do operando esquerdo e atribui o resultado ao operando esquerdo.
  ```java
  a -= b;  // Equivalente a a = a - b;
  ```

- **Atribuição multiplicativa** (`*=`): Multiplica o operando esquerdo pelo operando direito e atribui o resultado ao operando esquerdo.
  ```java
  a *= b;  // Equivalente a a = a * b;
  ```

- **Atribuição divisiva** (`/=`): Divide o operando esquerdo pelo operando direito e atribui o resultado ao operando esquerdo.
  ```java
  a /= b;  // Equivalente a a = a / b;
  ```

- **Atribuição de módulo** (`%=`): Calcula o resto da divisão do operando esquerdo pelo operando direito e atribui o resultado ao operando esquerdo.
  ```java
  a %= b;  // Equivalente a a = a % b;
  ```

### Operador Ternário

O operador ternário é uma forma concisa de escrever uma instrução if-else. A sintaxe é:

```java
variavel = (condição) ? expressão1 : expressão2;
```

Exemplo:

```java
int a = 10;
int b = 20;
int maior = (a > b) ? a : b;  // Se a > b, então maior = a, senão maior = b;
```

### Conclusão

Os operadores em Java são ferramentas fundamentais que permitem a manipulação e comparação de dados. Eles são utilizados em praticamente todas as partes de um programa, desde simples cálculos matemáticos até complexas operações lógicas e bit a bit. Entender como cada operador funciona e quando usá-los é crucial para a programação eficiente em Java.
