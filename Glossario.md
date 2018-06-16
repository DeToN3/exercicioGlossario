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

### Construtor
- É uma operação em uma classe responsável por criar um objeto.
usar codigo 

```java
public class Jedi{
public Jedi(){
} 
}

public class ChamarJedi {
 
 
public static void main(String[] args) { 
Jedi Yoda = new Jedi(); 
}
}
```

### Instanciação
- É um processo no qual se realiza a cópia de um objeto (classe) existente. Uma classe, a qual tem a função de determinar um tipo de dado, deve ser instanciada para que possamos utilizá-la. Assim criamos sua instância, onde definimos como sendo um objeto referente ao tipo de dado que foi definido pela classe. 

''' java
public class Jedi{
public string nome;
public string planeta;
}

public class StarWars{
static void Main(){
Jedi Luke = new Jedi();
Luke.nome = "Luke Skywalker";
Luke.planeta = "Tatooine";
Console.WriteLine(objPessoa.nome);
}          
}


