### Origem da linguagem Java
#origem
 Java foi criado por *James Gosling*, *Patrick Naughton*, *Chris Warth*, *Ed Frank* e *Mike Sheridan* em 1991. No inicio ela se chamava "Oak", mas foi renomeada como Java em 1995.

O Java não teve sua origem por causa da Internet, mas sim porque eles queria uma linguagem que fosse capaz de rodar em vários dispositivos diferentes, porque todos os dispositivos rodavam programas em C++, logo precisavam de um compilador de C++ destinado a aquela #CPU específica, tornando caro e demorado para criar isso. O *Gosling* queria criar uma linguagem multi-plataforma que pudesse ser executado em várias #CPU's diferentes. Durante o período de desenvolvimento do Java veio uma força que fez com que a linguagem se adapta-se também, o #WWW(Wolrd Wide Web) fez ele começar a ser pensado para também se adequar a tal, porque se ele não tive-se sido pensado para a Web ele provavelmente seria somente uma linguagem que e utilizada em utensílios domésticos, mas acabou casando com a Web por ela também precisar de um programas portáteis. 

#### 1.1 Qual a relação entre Java, C e C++?

Java é um programa que herda a sintaxe do C e tem um modelo de objetos adaptado do C++. Devido a semelhança as pessoas falam que Java é uma "versão de C++ para Web", mas é errado pensar dessa forma porque, primeiramente C++ foi criado para resolver um determinado conjunto de problemas e Java foi criado para resolver outro determinado conjunto de problemas, apesar das suas semelhanças por causa do comportamento da linguagem em relação a C++.

#### 1.2 Qual a relação entre Java e C#?

Da mesma forma que Java e C e C++ coexistem, Java e C# coexistem. C# é uma linguagem criada pela Microsoft e  tem recursos que são equivalentes diretos do Java.

### Contribuições da linguagem para a Internet

Java se tornou famoso na Web pois resolveu dois problemas: #segurança e #portabilidade por meio da criação de #applet's, simplificando a programação Web de forma geral.

#### Applets Java
#applet 

O #applet foram feitos para ser transmitidos via Web, são programas pequenos que é usado para; exibir dados fornecido pelo #servidor, tratar dados ou até mesmo para funções simples.

Isso inovou a maneira que objetos podem ser transmitido via #ciberespaço. Em geral há duas categorias de objetos que são transmitidos por #ciberespaço, [[Informações Passivas]] e [[Programas Ativos]] ou dinâmicos. #applet são programas ativos, pois são programas dinâmicos de execução automática.

Mas como Java resolveu o problema da #segurança? e da #portabilidade?

#### Segurança 
#segurança 

O Java conseguiu fornecer isso confinando o #applet, para negar todos os acessos a maquina do cliente, assim podendo baixar sem nenhum problema.

#### Portabilidade
#portabilidade 

Esse aspecto foi um dos que deu fama ao Java foi a #portabilidade pois resolveu o problema de forma magistral, ter um compilador para cada #CPU era o que atrapalhava o crescimento da Web, então o Java criou o #bytecode.

#### O segredo do Java: Bytecode
#bytecode 

O segredo é que em vez de sair código executável, ele sai #bytecode que é um código extremamente otimizado projetado para ser executado por uma #JVM (*Java Virtual Machine*: que é o sistema de tempo de execução Java). A #JVM foi originalmente criada para ser um *interpretador de #bytecode*, se fosse complilado em linguagem nativa teria que criar um programa para cada tipo de #CPU.

Existe uma diferença entre o tempo de um programa interpretado e um compilado, mas em relação ao #bytecode  esse tempo é menor, porque ele é extremamente otimizado, sendo mais rápido que uma linguagem interpretada, mas não há nada que impeça do bytecode ter uma complilação dinâmica  para código nativo visando desempenho.

Logo após o lançamento do Java eles lançaram o HotSpot que oferece um compilador #JIT(just-in-time) para #bytecode, o #JIT ajuda porque ele compila partes selecionadas, fragmento por fragmento. Não é pratico compilar o programa inteiro porque o Java tem validações que são feitas em tempo de execução, assim o #JIT compila so o necessário. Mesmo com o #JIT os princípios de #segurança e #portabilidade ainda são aplicáveis por ser rodado dentro de um ambiente controlado(JVM).

![[Java para Iniciantes/Capitulo 1/Imagens/Capitulo 1 - Fundamentos da linguagem Java.png]] ![[Capitulo 1 - Fundamentos da linguagem Java 1.png]]

### O jargão Java

As conciderações-chave do Java.

![[Capitulo 1 - Fundamentos da linguagem Java 2.png]]


### Programação Orientada a Objetos

#OOP pegou as melhores ideias da programação estruturada e combinou com conceitos novos. Existem de modo geral duas maneiras: a partir do código("o que está ocorrendo") ou a partir dos dados("o que está sendo afetado").

#Programação_estruturada são organizadas a partir do código, baseando "o código atuando sobre os dados".

#OOP é o contrario, são organizadas a partir dos dados, com principio chave: "dados controlando o acesso ao código", então basicamente, um tipo de dado define que tipo de operação pode ser aplicada a esses dados.

Devido a isso as linguagens de #OOP tem suporte a três coisas, #encapsulamento, #polimorfismo e #herança.

#### Encapsulamento
#encapsulamento 

O #encapsulamento encapsulamento é um mecanismo que vincula código e dados que são tratados. A unidade básica de encapsulamento do Java é a #classe, que por sua vez como é o que define forma a um #objeto, definindo a forma que os dados que operarão sobre ele e código também. O #objeto por sua vez é uma instância de uma #classe.

Códigos e dados que fazem parte de uma #classe são chamados de *membro* da #classe, os dados definido pela #classe são chamada de *variáveis membro* ou *variáveis de instância*. O código que opera sobre esses dados são chamados de *método membro* ou apenas #método(método é o termo em Java para uma sub-rotina).   

#### Polimorfismo
#polimorfismo 

