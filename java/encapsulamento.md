## Encapsulamento em Java

Encapsulamento é um dos quatro pilares da programação orientada a objetos (POO), ao lado de herança, polimorfismo e abstração. O encapsulamento refere-se à prática de esconder os detalhes internos de um objeto e expor apenas as funcionalidades essenciais. Isso ajuda a proteger os dados do objeto contra acesso indevido e manipulação, além de tornar o código mais modular e fácil de manter.

### Conceito Básico

Em Java, o encapsulamento é implementado através do uso de modificadores de acesso para restringir o acesso a variáveis e métodos dentro de uma classe. Os modificadores de acesso comuns são:

- **public**: acessível de qualquer lugar.
- **private**: acessível apenas dentro da própria classe.
- **protected**: acessível dentro do mesmo pacote e por subclasses.
- **default** (sem modificador): acessível apenas dentro do mesmo pacote.

### Benefícios do Encapsulamento

- **Segurança**: Protege os dados do objeto contra acesso não autorizado e manipulação incorreta.
- **Modularidade**: Facilita a manutenção e modificação do código, pois os detalhes internos de uma classe estão ocultos.
- **Flexibilidade**: Permite alterar a implementação interna sem afetar o código que utiliza a classe.
- **Reutilização**: Promove a reutilização do código, pois as classes encapsuladas podem ser usadas como blocos de construção em diferentes partes do programa.

### Exemplo de Encapsulamento

A seguir, um exemplo de como implementar o encapsulamento em Java. A classe `Pessoa` tem atributos privados e métodos públicos para acessar e modificar esses atributos.

#### Classe `Pessoa`

```java
public class Pessoa {
    // Atributos privados
    private String nome;
    private int idade;

    // Construtor
    public Pessoa(String nome, int idade) {
        this.nome = nome;
        this.idade = idade;
    }

    // Métodos getter para acessar os atributos
    public String getNome() {
        return nome;
    }

    public int getIdade() {
        return idade;
    }

    // Métodos setter para modificar os atributos
    public void setNome(String nome) {
        this.nome = nome;
    }

    public void setIdade(int idade) {
        if (idade > 0) {
            this.idade = idade;
        } else {
            System.out.println("Idade inválida!");
        }
    }
}
```

#### Classe `Main`

```java
public class Main {
    public static void main(String[] args) {
        // Criando um objeto da classe Pessoa
        Pessoa pessoa = new Pessoa("João", 25);

        // Acessando atributos usando métodos getter
        System.out.println("Nome: " + pessoa.getNome());
        System.out.println("Idade: " + pessoa.getIdade());

        // Modificando atributos usando métodos setter
        pessoa.setNome("Maria");
        pessoa.setIdade(30);

        // Acessando novamente para ver as alterações
        System.out.println("Nome: " + pessoa.getNome());
        System.out.println("Idade: " + pessoa.getIdade());

        // Tentando definir uma idade inválida
        pessoa.setIdade(-5);  // Isso imprimirá "Idade inválida!"
    }
}
```

### Explicação do Exemplo

- **Atributos Privados**: Os atributos `nome` e `idade` são privados, o que impede o acesso direto a eles de fora da classe `Pessoa`.
- **Métodos Getter e Setter**: Métodos públicos `getNome`, `getIdade`, `setNome` e `setIdade` são fornecidos para permitir acesso controlado aos atributos. Isso permite validação de dados, como no método `setIdade`, que verifica se a idade é maior que zero antes de atribuí-la.
- **Construtor**: O construtor é usado para inicializar os atributos ao criar uma nova instância da classe `Pessoa`.

### Encapsulamento com Atributos Calculados

Em alguns casos, os métodos getter podem calcular valores dinamicamente com base em outros atributos.

#### Exemplo

```java
public class Retangulo {
    private double largura;
    private double altura;

    public Retangulo(double largura, double altura) {
        this.largura = largura;
        this.altura = altura;
    }

    public double getLargura() {
        return largura;
    }

    public void setLargura(double largura) {
        this.largura = largura;
    }

    public double getAltura() {
        return altura;
    }

    public void setAltura(double altura) {
        this.altura = altura;
    }

    // Método getter para calcular a área
    public double getArea() {
        return largura * altura;
    }
}
```

#### Classe `Main`

```java
public class Main {
    public static void main(String[] args) {
        Retangulo retangulo = new Retangulo(5, 10);
        System.out.println("Largura: " + retangulo.getLargura());
        System.out.println("Altura: " + retangulo.getAltura());
        System.out.println("Área: " + retangulo.getArea());

        retangulo.setLargura(7);
        retangulo.setAltura(8);
        System.out.println("Área atualizada: " + retangulo.getArea());
    }
}
```

Neste exemplo, a classe `Retangulo` tem métodos getter e setter para os atributos `largura` e `altura`, e um método `getArea` que calcula a área do retângulo com base nesses atributos. Isso demonstra como o encapsulamento pode ser usado para fornecer acesso controlado a cálculos derivados de atributos.

### Conclusão

O encapsulamento é um princípio fundamental da programação orientada a objetos que promove a segurança, modularidade, flexibilidade e reutilização do código. Em Java, ele é implementado usando modificadores de acesso para restringir o acesso direto aos atributos e fornecer métodos públicos para acesso e modificação controlados.
