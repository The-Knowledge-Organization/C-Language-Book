# Expressões 

## Introdução
 O arquivo atual é exclusivamente sobre as expressões e a estrutura de uma expressão na linguagem C. 

## Expressões 
 Expressões são um conjunto de tipos, váriaveis, constantes, modificadores, funções e especificadores que juntos formam o que chamamos de expressão. 

```c
int main(void){
	static int stc; /* Expressão com um modificador de tipo de acesso, do tipo inteiro chamada de "stc". */
	return 0;
}
```

## **Tipos básicos**
 Tipos básicos servem para definirem como as funções, váriaveis, paramêtros formais e expressões serão lidas para o compilador.
___

**int**  
 O tipo "int" define a váriavel pra aceitar especificamente os números decimais mas suporta caracteres o que não é recomendável por causa 
do tamanho de 4 bytes para definir apenas um único caractere.

```c
int fn; /* Váriavel global "fn" é do tipo "int". */

/* Função "main" é do tipo "int", essa função executa todo o programa. */
int main(void){		
    int nu = 100; /* Váriavel "fun" é do tipo "int", é uma váriavel local que possui um valor atribuido "100". */
    int chr = 'a'; 
}
```

**char**  
 O tipo "char" define a váriavel pra armazenar especificamente caracteres, é possivel armazenar números decimais mas com muita limitação 
devido ao seu tamanho de 1 byte.

```c
int main(void){
	char str = 'i'; /* Váriavel "char str" tem atribuido o caractere 'i'. */
	char num = 100;	/* Variavel "char num" tem o valor atruibuido 100. */
}
```

**void**  
 O tipo "void" define a váriavel como nula, vazia, sem valor.

```c
/* função "main" contém no seu parâmetro o tipo "void", ou seja parâmetro nulo. */
int main(void){			
	void *p1; /* váriavel de ponteiro "*p1" é do tipo "void". */
}
```

**float**  
 O tipo "float" define a váriavel para armazenar números decimais de ponto flutuante, é recomendado se utilizar números de ponto flutuante 
devido ao seu tamanho de 4 bytes. 

```c
int main(void){
	float fnum = 10.123;
}
```

**double**  
O tipo "double" define a váriavel para suportar o dobro de casas decimais que o tipo "float", seu tamanho é de 8 bytes.

```c
int main(void){
	double dnum = 20.123;
}
```

### **Modificadores de tipos** 
 Modificam a maneira como cada tipo básico define as váriaveis, os modificadores se aplicam apenas aos tipos int, char, float e double e em 
casos específicos são úteis para reduzir os bits de um tipo básico e especificar melhor o que determinado tipo suportará o que economiza 
recursos em máquinas que não tem muito processamento.

**signed**  
 O modificador de tipos "signed" define que os tipos sejam modificados para suportar números decimais positivos e negativos.

```c
int main(void){
	signed int x = -10;
	signed int y = 20;
}
```

**unsigned**  
 O modificador de tipos "unsigned" define que os tipos sejam modificados para suportar apenas números decimais positivos. 

```c
int main(void){
	unsigned int y = 91;
}
```

**long**  
 O modificador de tipos "long" define uma modificação que aumenta o valor suportado do tipo utilizado e seus bits.

```c
int main(void){
	long int z = 100; /* int de 64 bits. */
	long double numf = 123.45; /* double de 128 bits. */
}
```

**short**  
 O modificador de tipos "short" define uma modificação que diminui o valor suportado do tipo utilizado e seus bits.

```c
int main(void){
	short int z = 10000; /* int de 16 bits. */
}
```

## **Modificadores de tipo de acesso** 
 Modificam como as expressões serão covertidas e modificadas pelo compilador.

**const**
 O modificador de acesso "const" define a expressão como apenas-leitura (Read-Only).

```c
int main(void){
	const int rov;
	return 0;
}
```

**volatile** 
 O modificador de acesso "volatile" define que a expressão pode ser modificada não explicitamente.

```c
int main(void){
	volatile char mut;
	return 0;
}
```
## **Especificadores de tipos de classe de armazenamento**
 Especificam para o compilador a maneira que cada expressão é armazenada.

**auto**  
 O especificador "auto" indica pro compilador que a váriavel não está com a duração de armazenamento definida, então o compilador define automáticamente a duração do 
armazenamento, "auto" é um especificador que existe para compatibilidade com a linguagem B e que não tem muita utilidade atualmente. 

```c
int main(void){
	auto int hello;
	return 0;
}
```

**register**  
 O especificador "register" registra a expressão no registrador da C.P.U (que é mais rápido) ou da memória R.A.M (que é mais lento), dependendo do tamanho pode ter um possivel
destaque de desempenho maior em expressões que contém os tipos básicos "int" e "char".

```c
int main(void){
	register char str;
	return 0;
}
```

**static**  
 O especificador "static" retém o valor entre chamadas de funções quando a expressão tem váriavel local e no caso de expressões com váriaveis globais o seu valor é retido apenas 
no arquivo sendo trabalhado.

```c
int main(void){
	static int num;
	return 0;
}
```

**extern**  
 O especificador "extern" buscará pelo diretório atual a váriavel determinada no código trabalhado.  

 Código do arquivo /projetos/**hello.c** 

```c
int abc;	/* váriavel global "abc". */

int main(void){
	int hi;	
	return 0;
}
```

 Código do arquivo /projetos/**hello2.c**

```c
extern abc;		/* váriavel global "abc" do arquivo "hello.c" utilizada no programa atual trabalhado. */

int main(void){
	abc = 123;
	return 0;
}
```

## **Operadores**
 Os operadores exercem funções em diversos operandos como váriaveis, funções, arrays e até expressões, cada operador tem uma função especifica e nisso pode operar como sendo 
unário, binário ou ternário.

**atribuição**  
 O operador de atribuição "=" atribui ao operando um valor desde números, 'caractere', "strings" e até expressões.

```c
int main(void){
	int x, y, z;	
	x = y;			/* atribuição uníca onde "x" tem seu valor atribuido de "y". */
	x = y = z;		/* atribuição multipla onde "x" tem seu valor atribuido de "y" e o mesmo tem o valor atribuido de "z". */
	return 0;
}
```

#### **Operadores aritiméticos** 
 Os operadores aritiméticos são amplamente utilizados em casos que necessitam de calculos, como no caso de números e expressões que contém multiplos valores, váriaveis ou 
expressões, os operadores aritiméticos em sua maioria seguem a "tabela de sinais" utilizada em matemática.

**Adição**  
 O operador aritimético de adição "+" especificará o operando como positivo ou efetua calculos de adição. 

```c
int main(void){
	int a, b, c; 
	c = a + b;		/* Váriavel "a" + "b"*/
	a = a + b;		/* Váriavel "a" tem seu valor atribuido "a" + "b". */
	a += b;			/* Forma abreviada da expressão acima. */
	return 0;
}
```

**Subtração**  
 O operador aritimético de subtração "-" especificará o operando como negativo ou efetua calculos de subtração.

```c
int main(void){
	int w, x, y, z;
	x = 100;
	y = -x;			/* Váriavel "y" tem o valor atribuido de "-x" que é "-100". */
	z = -y;			/* Váriavel "z" tem o valor atribuido de "-y" que é "100". */
	w = x - z;  	/* Váriavel "w" tem o valor atribuido de "x" subtraido a "z". */
	x = x - z;		
	x -= z;			
	return 0;
}
```

**Multiplicação**  
 O operador aritimético de multiplicação "*" serve para efetuar calculos de multiplicação com os operandos.

```c
int main(void){
	int x, y, z;	
	z = x * y;		/* Váriavel "z" tem o valor atribuido de "x" * "y". */
	x *= y;			
	return 0;
}
```

**Divisão**  
  O operador aritimético de divisão "/" serve para efetuar calculos de divisão com os operados.

```c
int main(void){
	int x, y, z
	z = x / y;
	x /= y;
	return 0;
}
```

**Modulo da divisão**  
 O operador aritimético do modulo da divisão "%" serve para mostrar o modulo/resto de um calculo de divisão. 

```c
int main(void){
	int x, y;
	x % y; 
	x %= y;
	return 0;
}
```

**Decremento**  
 O operador "--" opera sendo binário em expressões, váriaveis, decremento diminui em -1 o valor de determinado operando, e tem uma procedêcia 
diferente quando é usado como sufixo ou prefixo do operando.

```c
#include <stdio.h>

int main(void){
	int x = 10;
	printf("%d", --x);		/* subtração de -1 acontece antes, o valor de "x" é 9. */
	printf("%d", x--);		/* subtração de -1 acontece depois, o valor de "x" ainda é 9. */
	printf("%d", x);		/* o valor atual de "x" é 8. */
}
```

**Incremento**  
  O operador "++" opera sendo binário em expressões, váriaveis, incremento aumenta em +1 o valor de determinado operando, e tem uma procedência 
diferente quando é usado como sufixo ou prefixo do operando.

```c
#include <stdio.h>

int main(void){
	int y = 5;
	printf("%d", ++y);		/* O incremento acontece antes. o valor de "y" é 6. */
	printf("%d", y++);		/* O incremento acontece depois. o valor de "y" ainda é 6. */
	printf("%d", y);		/* O valor atual de "y" é 7. */
}
```

#### **Operadores relacionais** 
 Os operadores relacionais são utilizados em casos que são necessários fazerem alguma relação, comparação entre os operandos definidos e o operador.

**Operador "maior que.."**  

```c
int main(void){
	x > y;		/* "x" é maior que "y". */
	return 0;
}
```

**Operador "maior que ou igual.."**  

```c
int main(void){
	x >= y;		/* "x" maior ou igual a "y". */
	return 0;
}
```

**Operador "menor que.."**  

```c
int main(void){
	x < y;		/* "x" menor que "y". */
	return 0;
}
```

**Operador "menor ou igual.."**   

```c
int main(void){
	x <= y;		/* "x" menor ou igual a "y". */
	return 0;
}
```

**Operador "igual a.."**  

```c
int main(void){
	x == y;		/* "x" igual a "y". */
	return 0;
}
```

**Operador "diferente de.."**  

```c
int main(void){
	x != y; /* "x" diferente de "y".*/	
	return 0;
}
```

### **Operadores lógicos**
 Operadores lógicos estabelecem uma lógica específica que determina como os operandos e as expressões se conectarão com os outros.

**And**      
 O operador lógico "&&" determina que ambos os operandos devem ter a mesma lógica para ser verdadeiros.

```c
int main(void){
	10 != 9 && 20 < 21;		/* a lógica de âmbos é verdadeira. */
	10 == 9 && 13 < 22;		/* a lógica de um é falso e do outro é verdadeiro. */
	return 0;
}
```

**Or**  
 O operador lógico "||" determina que apenas um dos operandos precisa ser lógico para a expressão ser verdadeira.

```c
int main(){
	int x = 10, y = 1;
	x == y || 20 < 21;		/* a lógica de um deles é falsa e a outra é verdadeira. */
	x == y || 20 != 20;		/* a lógica de um deles é verdadeira e a outra é falsa. */
	return 0;
}
```

**Not**  
 O operador lógico not "!" determina que apenas um operando é necessário para operar e pode ser verdadeiro ou falso.

```c
int main(void){
	int x = 20, y = 10;
	x != y; 			/* a lógica aqui é verdadeira. */
	x == !(y + y); 		/* a lógica é falsa. */
	return 0;
}
```

### **Operadores Bit-a-Bit** 
Operadores bit-a-bit servem para atribuir, deslocar bits em bytes ou strings apenas int e char, cada um contém sua "tabela verdade".

**And (&)** 
O operador bit-a-bit and "&" desativa o bit de paridade, "and" bit-a-bit é similar ao and lógico.

```c
 1100 0001	/* valor de "x" em binário. */
 0111 1111	/* 127 em binário. */
&
 0100 0001	/* "x" sem paridade. */
```

**Or ( | )** 
Ativa os bits com quando é comparado "or" bit-a-bit é similar ao or lógico.

128|3;
```c
 1000 0000 /* 128 em binário. */
 0000 0011 /* 3 em binário.   */
|
 1000 0011 /* 131 em binário. */
```


**Or exclusivo (XOR) ( ^ )**
Ativa os bits quando apenas os comparados são diferentes.

127^120;
```c
 0111 1111 /* 127 em binário. */
 0111 1000 /* 120 em binário. */
^
 0000 0111 /* 7 em binário.   */
```

**Complemento de um ( ~ )**
Inverte o estado atual dos bits.
```c
 1110 0110 /* byte original                */
 0001 1001 /* após o primeiro complemento. */
 1110 0110 /* após o segundo complemento.  */
```


**Deslocamento a esquerda ( << )**
Deslocará bits para a esquerda e adicionarará zeros aos da direita.

```c
/*
 * "y" tem seu valor atribuido a 7 e se deslocará
 * apenas 1 bit a esquerda.
 */
x = y<<1;

0000 0111 /* 7 em binário e antes da deslocação. */
0000 1110 /* 14 em binário e após a deslocação.  */
```


**Deslocamento a direita ( >> )**
Deslocará bits para a direita e adicionarará zeros aos da esquerda.
```c
/*
 * "y" tem seu valor atribuido a 14 e se deslocará
 * apenas 1 bit a direita.
 */
x = y>>1;

0000 1110 /* 14 em binário e antes da deslocação. */
0000 0111 /* 7 em binário e após a deslocação.    */
```


### Operador ternário(:?)

Serve para substituir o if-else em casos específicos, utiliza expressões assim como if-else.

```c
// Se "x" é igual a "y" então "y", caso não, "z".
x == y ? y : z; 

/* 
 * Se "x" é igual a 200, então 2 * 5 * 20
 * caso contrário, 0.
 */
int result = x == 200 ? 2 * 5 * 20 : 0; 
```

### **Ponteiros**
Devolvem endereço ou valor na memória do operando, referênciam elementos de uma array (matriz), modifica os parâmetros das chamadas de função e suporta listas encadeadas e estruturas dinâmicas de dados.

**And ( & )**
Devolve o endereço da memória do operando.

```c
int a, b;

/*
 * "b" está atribuindo o pointeiro que devolve
 * o endereço da memória de "a".
 */
b = &a; 
```

**"Asterisco" ( * )**
Devolve o valor localizado no endereço de memória do operando.

```c
int *a = 10, b;
 /*
  * Váriavel "b" tem seu valor atribuido
  * o pointeiro de "a" que é contém o valor 10.
 */
b = *a;
```

### **Operador de tamanho**

Devolve o tamanho ocupado na memória por determinado operando.

**sizeof**   
Devolve o tamanho em bytes do operando incluido no parâmetro formal do operador.

```c
// int corresponde a 32 bits ou 4 bytes.
printf("tamanho de int é: %d bytes\n", sizeof (int)); 

/* =========================
 * OUTPUT =>
 * tamanho de int é: 4 bytes  
*/
```

### Operador de encadeamento

**Virgula ( , )**  
 Encadeaia multiplos operandos, no lado esquerdo do operador
será tratado como void, o lado direito torna-se o valor de toda a expressão.

```c
int x, y, z; /* Define "x" como inteiro, depois "y" e "z". */
x = (y = 10, z = 20, y + z); /* "x" tem seu valor atribuido a partir da expressão dentro de parênteses. */
```

### Operadores de referência  
Referenciam individualmente os elementos de um struct ou union.

**Ponto ( . )**  
O operador vai referenciar um elemento de um struct ou um union, abaixo um exemplo de um struct.

```c
/* "variant" é um identificador desse struct. */
struct variant{
    int a;
	char b[9];
} var; /* "var" é uma váriavel do struct "variant". */

/* Váriavel de um struct chamada "var" está referênciando o elemento "a" que tem ser valor atribuido 120. */
var.a = 120;  			
```

**Seta ( -> )**  
O operador servirá para referenciar um ponteiro de uma "struct".

```c
/* Ponteiro do valor de "p" tem seu valor atribuido  ao ponteiro do endereço de "var". */
struct variant *p = &var;

// O ponteiro "p" está atribuindo "abc" o valor 120;
p->abc = 120; 
```

### Operador de array (matriz)
Lista que contém ou não elementos incluidos, todos os elementos são mesmo tamanho e de valor fixo, arrays podem ser mutáveis.

**Colchetes ( [] )**
O operador realiza a indexação de arrays sobre o operando, onde é possivel aplicar determinada 
quantidade de elementos dentro da array dessa váriavel.

```c
char str[100];	/* listamos 100 elementos dentro da array de "str". */

/* Array vazia tem elementos pré-definidos pelo compilador, 
 * a array de "hi" tem um "string" atribuido "hello".*/
char hi[] = "hello"; 	
```

### Operador Cast

**Cast** 
O operador cast "(tipo)" forçará determinada expressão a utilizar um tipo especificado entre parênteses. 

```c
#include <stdio.h>
int main(void){
	int i = 1;
	
	/* float entre parênteses força
	 * o número a não ser um inteiro na saída.
	 */
	printf("value of i / 2 is %f"(float) i / 2); 	
	return 0;
}
```
### **Resumo das precedências dos operadores e como operam**
 A tabela mostra qual é a maior precedência em uma ordem superior a inferior e em sequẽncia em cada linha,  
mostram a procedência em onde o da esquerda é o maior em relação ao da direita.

|			   Maior			|
|			   :--:				|
|		     () [] ->			|	
| ! ~ ++ -- - (cast) * & sizeof |
| 			  * / %				|
| 			  + -				|
| 			  << >>				|
| 		    < <= > >=			|
| 			  == !=				|
| 			    &				|
| 			    ^				|
| 			    !				|
| 			    &&				|
| 			    !!				|
| 			    ?:				|
| 		 = += -= *= /=etc.		|
| 			    ,				|
|			   Menor			|


|    Operadores    |   Operam como	 |
|	    :--: 	   |	   :--:		 |
|	     ()		   |	  binário	 |
|		 []		   |
|		 ->		   |
|		 !		   |
|		 ~		   |
|		 ++		   |
|		 --		   |
|	   (cast)	   |
|	     +	       |  binário/unário |
|	     -		   |  binário/unário |
|	     *		   |  binário/unário |
|        /		   | 	  binário 	 |
|        %		   |  binário/unário |
|        ++		   | 	  unário	 |
|	     --		   |	  unário	 |
|		 &		   |
|	   sizeof	   |
