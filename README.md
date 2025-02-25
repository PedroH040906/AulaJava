# Aula  Java

## Introdução ao Java
Java é uma linguagem de programação orientada a objetos e multiplataforma, conhecida por sua portabilidade e segurança. Foi criada pela Sun Microsystems (atualmente pertencente à Oracle) e é amplamente utilizada para o desenvolvimento de aplicações empresariais, web, mobile e desktop.

## Conceitos basicos

### O que é uma IDE?
IDE (Integrated Development Environment) é um ambiente de desenvolvimento integrado que facilita a escrita, compilação e depuração de código. Algumas IDEs populares para Java são:

- IntelliJ IDEA

- Eclipse

- NetBeans

- VS Code (com extensões)

### O que é JDK?

JDK (Java Development Kit) é o kit de desenvolvimento do Java, contendo tudo o que é necessário para programar nessa linguagem, incluindo:

- Compilador Java (javac)

- JVM (Java Virtual Machine)

- Bibliotecas padrão

###  O que é um Algoritmo?

Um algoritmo é um conjunto de passos lógicos e bem definidos para resolver um problema. No contexto da programação, um algoritmo pode ser implementado usando uma linguagem como Java.

### Introdução a variaveis

Uma variável é um espaço na memória do computador usado para armazenar um valor que pode ser modificado durante a execução do programa. Em Java, uma variável precisa ser declarada com um tipo, que define o tipo de dado que ela pode armazenar.

int → números inteiros (ex: int idade = 25;)
double → números decimais (ex: double altura = 1.75;)
String → texto (ex: String nome = "Pedro";)
boolean → verdadeiro ou falso (ex: boolean ativo = true;)
char → um único caractere (ex: char letra = 'A';)
BigDecimal → números decimais de alta precisão (ex: BigDecimal saldo = new BigDecimal("12345.67");)


### Arrays
Um array é uma estrutura que guarda vários valores do mesmo tipo dentro de uma única variável. Isso é útil quando precisamos armazenar e trabalhar com uma coleção de dados sem precisar criar várias variáveis separadas.

```
int[] numeros = new int[5];  // Criando um array com 5 posições

int[] numeros = {10, 20, 30, 40, 50};  // Criando e preenchendo o array ao mesmo tempo

int[] numeros = {10, 20, 30, 40, 50};
numeros[1] = 99;  // Mudando o valor da segunda posição para 99
System.out.println(numeros[1]); // Agora vai mostrar 99

```

### Camel Case

- **CamelCase** é um estilo de nomenclatura onde as palavras são concatenadas sem espaços, e a primeira palavra começa com letra minúscula, enquanto as palavras subsequentes começam com letra maiúscula.

### EX VARIAVEL
errado: int idade_Pessoa; / int Idadepessoa; / int IdadePessoa;

    certo: int idadePessoa; //todas as variaveis devem começar com letra minuscula e utilizar CamelCase.


### EX CLASSE
errado: pessoaFisica / Pessoa_Fisica / Pessoa Fisica / Pessoafisica

    certo: PessoaFisica; //todas as Classes devem começar com letra Maiuscula e utilizar CamelCase.




### Escopo e Chaves {} em Java

O escopo define onde uma variável ou bloco de código pode ser acessado dentro do programa. Em Java, usamos chaves {} para delimitar blocos de código, como em métodos, loops e estruturas condicionais.

#### Exemplo de escopo e uso de chaves:

public class Exemplo {
public static void main(String[] args) {
int x = 10; // Variável dentro do método main

        if (x > 5) {
            int y = 20; // Escopo limitado ao bloco do if
            System.out.println("X é maior que 5 e Y vale: " + y);
        }
        // System.out.println(y); // Isso daria erro, pois y está fora de escopo
    }
}
### Programação Orientada a Objetos (POO)
A Programação Orientada a Objetos (POO) é um paradigma de programação que organiza o software em "objetos", que são instâncias de classes. Esses objetos possuem atributos (também chamados de propriedades ou campos) e métodos (ou funções), que definem o comportamento dos objetos.

A POO é baseada em quatro pilares fundamentais:

1. Encapsulamento
   O encapsulamento é o processo de esconder os detalhes internos de um objeto e permitir o acesso a esses dados apenas através de métodos públicos. Isso garante que os dados de um objeto sejam acessados e modificados de maneira controlada, o que melhora a segurança e a manutenção do código.

```
public class Pessoa {
    // Atributos privados (encapsulados)
    private String nome;
    private int idade;

    // Método público para acessar o nome
    public String getNome() {
        return nome;
    }

    // Método público para modificar o nome
    public void setNome(String nome) {
        this.nome = nome;
    }

    // Método público para acessar a idade
    public int getIdade() {
        return idade;
    }

    // Método público para modificar a idade
    public void setIdade(int idade) {
        this.idade = idade;
    }
}
```

## Herança
A herança permite que uma classe herde os atributos e métodos de outra classe. Isso permite reutilizar código e criar hierarquias de classes. Uma classe que herda outra é chamada de subclasse (ou classe derivada), e a classe que é herdada é chamada de superclasse (ou classe base).

```
// Superclasse
public class Animal {
    public void fazerSom() {
        System.out.println("O animal faz um som.");
    }
}

// Subclasse
public class Cachorro extends Animal {
    @Override
    public void fazerSom() {
        System.out.println("O cachorro late.");
    }
}

```
No exemplo acima, a classe Cachorro herda a classe Animal, mas sobrescreve o método fazerSom() para exibir um som específico para o cachorro. A herança permite que a classe Cachorro tenha todas as características da classe Animal sem precisar reescrever tudo.

## Polimorfismo

O polimorfismo é o conceito de que um objeto pode assumir diferentes formas. Em Java, o polimorfismo é geralmente implementado por meio de sobrecarga de métodos (métodos com o mesmo nome, mas parâmetros diferentes) e sobrescrita de métodos (um método de uma classe filha que substitui o método da classe pai).

```
public class Animal {
    public void fazerSom() {
        System.out.println("O animal faz um som.");
    }
}

public class Gato extends Animal {
    @Override
    public void fazerSom() {
        System.out.println("O gato mia.");
    }
}

```
## Abstração
A abstração é o processo de ocultar os detalhes complexos e exibir apenas as informações essenciais. Ela permite que o programador se concentre no que o sistema faz, sem se preocupar com os detalhes de implementação. Em Java, a abstração é frequentemente alcançada através de interfaces e classes abstratas.

```
abstract class Animal {
    abstract void fazerSom(); // Método abstrato

    public void dormir() {
        System.out.println("O animal está dormindo.");
    }
}

class Cachorro extends Animal {
    @Override
    void fazerSom() {
        System.out.println("O cachorro late.");
    }
}

```
