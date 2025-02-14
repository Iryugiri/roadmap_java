### **Principais habilidades e conceitos**
• Saber os fundamentos da classe 
• Entender como os objetos são criados 
• Entender como as variáveis de referência são atribuídas 
• Criar métodos, retornar valores e usar parâmetros 
• Usar a palavra-chave return 
• Retornar um valor de um método 
• Adicionar parâmetros a um método 
• Utilizar construtores 
• Criar construtores parametrizados 
• Entender new 
• Entender a coleta de lixo e os finalizadores 
• Usar a palavra-chave this

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