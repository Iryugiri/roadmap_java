### **Principais habilidades e conceitos**
- [x] Saber os fundamentos da classe 
- [x]  Entender como os objetos são criados 
- [x]  Entender como as variáveis de referência são atribuídas 
- [x]  Criar métodos, retornar valores e usar parâmetros 
- [x]  Usar a palavra-chave return 
- [x]  Retornar um valor de um método 
- [x]  Adicionar parâmetros a um método 
- [x]  Utilizar construtores 
- [x]  Criar construtores parametrizados 
- [x]  Entender new 
- [x]  Entender a coleta de lixo e os finalizadores 
- [x]  Usar a palavra-chave this

## <span style="background:#d4b106">Definindo uma classe</span>
Desenvolveremos uma classe chamada *Vehicle* que conterá três informações sobre um veículo:
- o número de passageiros que ele pode levar;
- a capacidade de armazenamento de combustível;
- e o consumo médio de combustível (em milhas por galão).
A primeira versão da classe conterá apenas dados.
```Java
class Vehicle {
	int passengers;
	double fuelcap;
	double mpg;
}
```
Lembramos que uma declaração #classe é só uma descrição de tipo; ela não cria um objeto real. Logo, o código anterior não faz nenhum objeto de tipo *Vehicle* passar a existir.

Para criar um #objeto *Vehicle*, é necessário usar a instrução: 

```Java
Vehicle minivan = new Vehicle();
```

Após isso **minivan** será uma instância de *Vehicle*. Sempre que for criado uma instância de uma #classe, estará criando um #objeto contendo sua própria copia de cada #variavel de instância definida pela #classe. Para acessar a variável, usa-se o #operador **ponto** (**.**). O #operador ponto vincula o nome de um objeto ao nome de um membro: 

**objeto.membro**

Para atribuir o valor 16 a variável **fuelcap** de **minivan**:

```Java
minivan.fuelcap = 16;
```

## <span style="background:#d4b106">Como os Objetos são criados</span>

No tópico acima foi mostrado a instrução: 

```Java
Vehicle minivan = new Vehicle();
```

Essa declaração fa duas coisas: 

1° - Ela declara uma variável chamada **minivan** do tipo *Vehicle*, essa variável não define um objeto, ela pode apenas <span style="background:#40a9ff">referenciar</span> um objeto.

2° - A declaração cria uma copia física do objeto e atribui à **minivan** uma referência a ele. Isso é feito através do #operador **new**.

Essas duas etapas podem ser reescritas dessa forma para exemplificar: 

```Java
Vehicle minivan;
minivan = new Vehicle();
```

A primeira linha declara **minivan** como referência a um objeto de tipo *Vehicle*. Portanto, **minivan** pode referenciar um #objeto do tipo *Vehicle*, mas não é um objeto. Na próxima linha cria um novo objeto *Vehicle* e atribui à minivan uma referência a ele, assim vinculando um a var a um objeto.

## <span style="background:#d4b106">Variáveis de referência e a atribuição</span>

Em operações de atribuição, variáveis de referência agem diferente de variáveis do tipo primitivo. Quando a atribuição de variáveis é do tipo primitivo é simples, acontece uma copia de valor, a variável da esquerda recebe uma cópia do valor da direita. Mas quando é por referência acontece um "apontamento", porque alteramos o objeto para qual a variável de referência aponta. Por exemplo:

```Java
Vehicle car1 = new Vehicle();
Vehicle car2 = car1; 
```

Nesse caso, **car1** recebe um #objeto do tipo *Vehicle*, a primeira vista podemos imaginar que **car2** recebe um outro objeto, mas **car2** apenas começa a apontar para o mesmo espaço de memoria que **car1**, assim ele referenciam o mesmo objeto.

## <span style="background:#d4b106">Métodos</span>

### Forma geral: 
```Java
tipo-ret nome ( lista-parâmetros ) {
	// corpo do método;
}
```

### Usando parâmetros

Podemos passar um ou mais valores para um método quando ele é chamado. Um valor passado para um método se chama argumento. Dentro do método, a variável que recebe o argumento se chama parâmetro. Os parâmetros são declarados dentro dos parênteses que vêm após o nome do método.

### Retornando um Método

A instrução #return é "um palavra-chave do Java que retorna", ela pode retornar um void (métodos que não retornam valor) e os que retornam valor. 


## <span style="background:#d4b106">Construtores</span>

### Definição

Um #construtor **inicializa um objeto** quando este é criado. Ele tem o mesmo nome de sua classe e é sintaticamente semelhante a um #método. No entanto, os construtores **não têm um tipo de retorno explícito**. Normalmente, usamos um #construtor para fornecer valores iniciais para as variáveis de instância definidas pela classe ou para executar algum outro procedimento de inicialização necessário à criação de um objeto totalmente formado.

Todas as classes têm construtores, mesmo quando não definimos um, porque Java fornece automaticamente um construtor padrão que inicializa todas as variáveis membros com seus valores padrão, que são zero, #null e #false, para tipos numéricos, tipos de referência e booleans, respectivamente. No entanto, quando definimos nosso próprio construtor, o #construtor padrão não é mais usado.

### Forma Geral

```Java
modificador-de-acesso Nome-da-classe (Parametros) {
	escopo
}
```

## <span style="background:#d4b106">Operador New</span>

Forma Geral

```Java
var-classe = new nome-classe(lista-arg)
```

#new instância um construtor da classe, se não houver construtor ela instância um que é definido pelo proprio Java.

O operador #new retorna uma referência ao objeto recém criado.

## <span style="background:#d4b106">Garbage Colector</span>

A alocação de memória não é infinita, então é possível que o #new falhe por nao ter memória.

Em algumas linguagens isso é feito manualmente, mas em Java o sistema de coleta de lixo reclama os objetos automaticamente, sendo de maneira transparente em segundo plano.

Funciona assim: Quando não existe nenhuma referência a um objeto, ele não é mais considerado necessário e a memória ocupada é liberada, então  reciclando, podendo ser usada em uma alocação subsequente.

![[Capítulo 4 - Introdução a classes, objetos e métodos.png]]#ats

A coleta de lixo só ocorre esporadicamente durante a execução do programa. Ela não ocorrerá só porque existem um ou mais objetos que não são mais usados. A título de eficiência, geralmente o cletor de lixo só é executado quando duas condições são atendidas: há objetos a serem reciclados e há a necessidade de reciclá-los. Lembre-se, a coleta de lixo é demorada, logo, o sistema de tempo de execução Java só a executa quando apropriado. Portanto, não temos como saber exatamente quando ela ocorrerá.

### Método **finalize()**

É possível definir um método para ser chamado imediatamente antes da destruição final de um objeto pelo coletor de lixo. É importante entender que **finalize( )** é chamado imediatamente antes da coleta de lixo. Ele não é chamado quando um objeto sai de escopo, por exemplo. Ou seja, não temos como saber quando, ou até mesmo se **finalize( )** será executado. Por exemplo, se o programa terminar antes da coleta de lixo ocorrer, finalize( ) não será executado. Logo, ele deve ser usado como um procedimento “reserva” para assegurar o tratamento apropriado de algum recurso ou para aplicações de uso especial, e não como um artifício para o programa usar em sua operação normal.

## <span style="background:#d4b106">A palavra-chave this</span>

Quando um método é chamado, ele recebe automaticamente um argumento implícito, que é uma referência ao objeto chamador (isto é, o objeto em que o método é chamado).