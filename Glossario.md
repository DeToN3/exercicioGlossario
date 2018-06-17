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
<p>  +-----------------------+  </p>
<p>  '         Gato          '  </p>
<p>  '-----------------------'  </p>
<p>  '  Nome                 '  </p>
<p>  '  Peso                 '  </p>
   '  Raça                 '
   '-----------------------'
   '  +Miar                '
   '  +Andar               '
   +-----------------------+
