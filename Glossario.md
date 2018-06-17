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
