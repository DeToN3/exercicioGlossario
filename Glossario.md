# Glossário
- ##### Construtor
- ##### Instanciação
- ##### Palavra reservada new
- ##### Palavra reservada instanciof
- ##### Encapsulamento
- ##### Palavra reservada this
- ##### Getters/Setters
- ##### Palavra reservada public/private
- ##### Assinatura de método
- ##### Sobrecarga de método
- ##### Escopo de classe
- ##### Escopo de objeto
- ##### Palavra reservada final
- ##### Relacionamento de dependência
- ##### Relacinamento de Agregação
- ##### Relacionamento de Composição
- ##### Referências

## Construtor
- É uma operação em uma classe responsável por criar um objeto.

```java
public class Jedi{
/* Aqui está se criando o construtor */
public Jedi(){
} 
}

/*~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~*/

public class ChamarJedi {
 
 
public static void main(String[] args) { 
Jedi Yoda = new Jedi(); 
}
}
```

## Instanciação
- É um processo no qual se realiza a cópia de um objeto (classe) existente. Uma classe, a qual tem a função de determinar um tipo de dado, deve ser instanciada para que possamos utilizá-la. Assim criamos sua instância, onde definimos como sendo um objeto referente ao tipo de dado que foi definido pela classe. 

``` java

public class Jedi {
public String nome;
public String planeta;
}
 
/*~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~*/

public class Luke {
public static void Main(){
/* Aqui acontece a instanciação */
Jedi Luke = new Jedi();
Luke.nome = "Luke Skywalker";
Luke.planeta = "Tatooine";
}     
}
```
## Palavra reservada new
- Usada para chama o construtor do objeto e criar um objeto instanciado a uma classe.
#### Confira Exemplos em Construtor e Instanciação.

## Palavra reservada instanciof
- Determina se um objeto é a instancia de uma classe, superclasse ou interface.

``` java
Jedi Luke = new Jedi();
if (Luke instanceof Jedi){
System.out.println("A força está com você");
}else{
System.out.println("A força não está com você");
}
} 
```

## Encapsulamento
- Trata de organizar os dados que sejam relacionados, agrupando-os em objetos, reduzindo as colisões de nomes de variáveis (dado que variáveis com o mesmo nome estarão em namespaces distintos) e, da mesma forma, reunindo métodos relacionados às suas propriedades.

 <p> +-----------------------+ </p>                      
 <p> |         Gato          | </p>                   
 <p> |-----------------------| </p>              
 <p> |  nome                 | </p>                     
 <p> |  peso                 | </p>                      
 <p> |  raça                 | </p>                    
 <p> |-----------------------| </p>                       
 <p> |  +miar                | </p>                       
 <p> |  +andar               | </p>                       
 <p> +-----------------------+ </p>                       
 
 <p> +-----------------------+ </p>                       
 <p> |         Homem         | </p>
 <p> |-----------------------| </p>
 <p> |  nome                 | </p>
 <p> |  peso                 | </p> 
 <p> |  etnia                | </p>
 <p> |-----------------------| </p>
 <p> |  +falar               | </p>
 <p> |  +andar               | </p>
 <p> +-----------------------+ </p>
 
 Confira nos exemplos acima que os dois atributos possuem nomes iguais, porem o seu domínios se difere. Assim podemos acessar Gato.nome ou Homem.nome sem conflito. 
 
## Palavra Reservada This
- This é usado para referenciar uma variável a instancia atual de um objeto, ou seja, usado para fazer utilizar uma variável da classe na qual se está trabalhando.

``` java
public class Jedi {
String nome;

Jedi(String nome){
    this.nome = nome;
}
}

/*~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~*/

public class NewJedi {
public static void main(String[] args) {
    Jedi Anakin = new Jedi("Anakin Skywalker");
    System.out.println(Anakin.nome);
    //Então imprimi-se "Anakin Skywalker"
    }
}
```
Outro Exemplo: 
``` java
public class TESTE {
      String nome = "Marcelo";
    TESTE() {
        String nome = "Marcelo";
        if(this.nome == nome) {
            System.out.println("mesmo objeto");
        }
        else {
            System.out.println("Objetos diferentes");
    }
    }
}

/*~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~*/

public class TESTE2 {
    public static void main(String[] args){
        TESTE eu = new TESTE();
        //Neste caso é impresso "o mesmo objeto"
    }
    
}
```

## Getters/Setters
- Os getters e setters usados quando se quer encapsular uma classe, ou seja, os atributos privados dessa classe só poderão ser acessados por outras classes através desses métodos. Isso serve para controlar o acesso aos atributos da classe e é uma boa prática.

``` java
public class GetSet {
  private String nome = "Marcelo";
  public String getNome(){
  return nome;
  }
  public void setNome(String nome){
  this.nome = nome;
  }
}

/*~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~*/

public class GetSetmain {
    public static void main(String[] args){
        GetSet request = new GetSet();
        request.setNome("Arthur");
        System.out.println(request.getNome());
        //Neste caso será impresso Arthur, pois o set está dando um novo parâmetro
        
}
}
```
## Palavra reservada public/private
- Ambos são modificadores de acesso, suas diferenças implicam no grau de acesso. 
- Public torna a classe, método ou variável acessável a partir de qualquer classe. 
- Private segue a mesma idéia do Public, porém é acessável apenas dentro da própria classe.

## Assinatura de método
- Assinatura de método é a combinação do nome do método, tipo e a ordem dos parâmetros.

``` java
//                             Parâmetros   ←  
//                             ↑            ↑
public static double metodo(int num1, double num2){
//              ↓            ↓           ↓
//         Nome do método    ---------→Tipos
   double resultado = num1+num2;
   return resultado;
}
```

## Sobrecarga de método
- consiste em criar o mesmo método com possibilidades de entradas diferentes. Essas entradas (parâmetros) devem sempre ser de tipos diferentes, quantidades de parâmetros diferentes ou posições dos tipos diferentes.
Confira abaixo um exemplo com diferentes parâmetros e retornos.

``` java
public class Calculadora{
   public int soma (int num1, int num2){
      return num1+num2;
   }
   public int soma (int num1, int num2, int num3){
      return num1+num2+num3;
   }
   public double soma (double num1, double num2){
      return num1+num2;
   }
}
```

##Escopo de Classe 
-Referente a vida e acessibilidade de uma variável. Seu tamanho e alcance depende de onde uma variável é declarada. Por exemplo, se uma variável é declarada na parte superior de uma classe, ela será acessível a todos os métodos de classe. Se for declarada num método, em seguida, só pode ser utilizada em tal método.

``` java
public void teste(){//Começo do escopo
   int valor = 10;
   System.out.println("O valor é: ",valor);
}//Fim do escopo
```

## Escopo de objeto
- É o limite que um objeto pode manipular, visualizar ou acessar os atributos ou métodos dando ou não permissão (private, protected, public) para si p´roprio ou a bibliotecas externas para acessa-la.

```java
protected String nome;
public double valor;
private String senha;
```
## Palavra reservada final
- Quando usado na definição de uma variável, significa que ela não pode assumir outro valor, tornando-a uma constante. Quando usada na definição de um método, significa que o mesmo não poderá ser subescrito.

```java
public class POO{
   public final void aula(){}
}
public class SOP extends POO {
   public void aula(){} //Não é permitido sobrescrever o método
}
```
## Relacionamento de dependência
- É um relacionamento no qual um elemento, usa ou depende de outro elemento. Um relacionamento de dependência também pode ser utilizado para representar precedência, em que um elemento de modelo deve preceder outro. Ou seja ocorre quando usa os serviçoes de outra classe.

## Relacinamento de Agregação
- Ocorre quando há uma relação todo parte, onde a parte pode existir sem o todo. 

## Relacinamento de Composição
- Ocorre quando há uma relação todo parte, onde a parte não existe sem o todo.


## Referências
<p> <https://www.devmedia.com.br>
<p> <http://www.dca.fee.unicamp.br/cursos/PooJava/desenvolvimento/umlclass.html> </p>
<p> <https://desenvolvimentoaberto.org/2014/02/14/classes-escopos-java-c-e-c/> </p>
<p> <http://www.nacaolivre.com.br/javascript/escopo-de-objeto-em-javascript/> </p>
<p> <https://www.ibm.com/support/knowledgecenter/pt-br/SS8PJ7_8.5.1/com.ibm.xtools.modeler.doc/topics/cdepend.html> </p>
