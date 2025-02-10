**Principais habilidades e conceitos**
• Conhecer os tipos primitivos de Java 
• Usar literais 
• Inicializar variáveis 
• Saber as regras de escopo de variáveis dentro de um método
• Usar os operadores aritméticos
• Usar os operadores relacionais e lógicos 
• Entender os operadores de atribuição 
• Usar atribuições abreviadas 
• Entender a conversão de tipos em atribuições 
• Converter tipos incompatíveis
• Entender a conversão de tipos em expressões

### Tipo primitivos de Java

![[Java para Iniciantes/Capitulo 2/Imagens/Capitulo 2 - Introdução a tipo de dados e operadores.png]]

#### Inteiros

Existem 4 tipo de #inteiros, #byte,#short,#int,#long

![[Capitulo 2 - Introdução a tipo de dados e operadores 1.png]]

Como mostrado na imagem acima Java não suporta inteiros sem sinais(somente positivos).

Tecnicamente, em tempo de execução, Java pode usar qualquer tamanho para armazenar  um tipo primitivo, mas os tipos deve agir como especificado.

![[Capitulo 2 - Introdução a tipo de dados e operadores 2.png]]
#ats

#### Ponto Flutuante

Existem dois tipos de ponto flutuante #float e #double, sendo o primeiro com 32 bits e o segundo com 64 bits. 

O double é mais usado por ser o tipo que a #classe padrão do *Math* retorna. 

#### Caracteres

Em Java, os caracteres não são armazenados em 8 bits como em outras linguagens. O Java usa o #unicode, ele define um conjunto de caracteres que podem representar todos os caracteres encontrados em todos os tipos de idiomas. O #char é um tipo de 16 bits (sem sinal) cobre um intervalo de 0 a 65,536. A tabela #ASCII, sendo um subconjunto do #unicode, usa 8 bits por padrão cobrindo um intervalo de 0 a 127.

<span style="background:#ff4d4f">NOTA</span>: quando atribuímos um valor a um #char em Java usamos *'* *'* .

Ja que #char é um tipo de 16 bits sem sinal, podemos fazer a seguinte coisa:

```Java
class CharArithDemo {
	public static void main(String args[]) {
		char ch;
		ch = 'X';
		System.out.println("O valor do char e: " + ch);

		ch++; // Incrementa o ch
		System.out.println("O valor do char e: " + ch);

		ch = 90; // Dá o ch o valor Z
		System.out.println("O valor do char e: " + ch);
	}
}
```

Na linha 51 podemos ver que o #char *pode* ser incrementado e na linha 54 podemos ver que foi atribuído o valor 90, que no valor da #ASCII( e do #unicode, ja que os 127 primeiros valores são iguais a da #ASCII ).

![[Capitulo 2 - Introdução a tipo de dados e operadores 3.png]] #ats

#### Booleano

O tipo #boolean recebe os valores verdadeiro ou falso.


### Exercício

Neste projeto, você criará um programa que calcula a que distância, em pés,
um ouvinte está da queda de um relâmpago. O som viaja a aproximadamente 1.100 pés por segundo pelo ar. Logo, conhecer o intervalo entre o momento em que você viu um relâmpago e o momento em que o som o alcançou lhe permitirá calcular a distância do relâmpago. Para este projeto, assuma que o intervalo seja de 7,2 segundos.

Resolução:

![[Sound.java]]

#### Literais
#literal

Em java os #literal são valores fixos representados em sua forma legível por humanos. Os literais são qualquer tipo de dado primitivo e a maneira de ser representado depende do tipo. As constantes no Java são  representada por *'* *'*, por exemplo 'a' e '%' são constantes de caracteres. Por padrão, os #inteiros são declarados simplesmente colocando o numero e os #long são declarados acrescentando um L na frente do número. Por exemplo: 12 é um inteiro, mas 12L é um #long.

Embora os literais inteiros criem um valor int por padrão, eles podem ser atribuídos a variáveis de tipo char, byte ou short contanto que o valor atribuído possa ser representado pelo tipo de destino. Um literal inteiro sempre pode ser atribuído a uma variável long.

A partir do JDK 7, é permitido embutir um ou mais sublinhados em um literal inteiro ou de ponto flutuante. Isso pode facilitar a leitura de valores compostos por muitos dígitos. Quando o literal é compilado, os sublinhados são simplesmente descartados. Aqui está um exemplo:

123_34_1234

Essa linha especifica o valor 123.451.234. O uso de sublinhados é particularmente útil na codificação de coisas como números de peças, identificações de clientes e códigos de status que normalmente são criados como uma combinação de subgrupos de dígitos.

### Literais hexadecimais, octais e binários

Sistemas baseados em 8 ou 16 em vez de 10 normalmente são mais fáceis de usar na programação.

O sistema numérico baseado em 8 se chama #octal, onde o número 10 é igual ao 8 do sistema decimal. Já o com base 16 se chama #hexadecimal e usa o dígitos de 0 a 9 mais letras de A a F, que representam 10,11,12,13,14,15.

O Java permite a especificação de literais inteiros em #hexadecimal e em #octal em vez de decimal. 

Para #literal #hexadecimal basta colocar um 0x ou 0X antes do número:

```Java
hex = 0xFF // 255 em decimal
```

Para #literal #octal basta colocar um 0 antes do número:
```Java
oct = 011 // 9 em decimal
```

A partir do Java 7 é possível usar #literal inteiro para uso #binário. Para fazer isso basta usar um `0b` ou `0B`: 

**Exemplo dos casos abaixo:**

![[Literais.java]]

<font color="#ff0000">Return:</font>
Esse é o valor 0xFF em hexadecimal: 255
Esse é o valor 011 em octal: 9
Esse é o valor 1100 em binario: 12