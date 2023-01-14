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

###  **Operadores Bit-a-Bit** 
 Operadores bit-a-bit servem para atribuir, deslocar bits em bytes ou strings apenas int e char, cada um contém sua "tabela verdade".

**And**  
 O operador bit-a-bit and "&" desativa o bit de paridade, "and" bit-a-bit é similar ao and lógico.

```c
 1100 0001	/* valor de "x" em binário. */
 0111 1111	/* 127 em binário. */
&
 0100 0001	/* "x" sem paridade. */
```

Or ( | ): ativa os bits com quando é comparado "or" bit-a-bit é similar ao or lógico.
```c
```
128|3;

 1000 0000 /* 128 em binário.
 0000 0011 /* 3 em binário.
|
 1000 0011 /* 131 em binário.


Or exclusivo (XOR) ( ^ ): ativa os bits quando apenas os comparados são diferentes.
```c
```
127^120;

 0111 1111 /* 127 em binário.
 0111 1000 /* 120 em binário.
^
 0000 0111 /* 7 em binário.


Complemento de um ( ~ ): inverte o estado atual dos bits.
```c
```
 1110 0110 /* byte original
 0001 1001 /* após o primeiro complemento.
 1110 0110 /* após o segundo complemento.


Deslocamento a esquerda ( << ): deslocará bits para a esquerda e adicionarará zeros aos da direita.
```c
```
x = y<<1; /* "y" tem seu valor atribuido 7 e se deslocará apenas um bit a esquerda.
0000 0111 /* 7 em binário e antes da deslocação.
0000 1110 /* 14 em binário e após a deslocação.


Deslocamento a direita ( >> ): deslocará bits para a direita e adicionarará zeros aos da esquerda.
```c
```
x = y<<1; /* y tem seu valor atribuido 14 e se deslocará apenas um bit a direita.
0000 1110 /* 14 em binário e antes da deslocação.
0000 0111 /* 7 em binário e após a deslocação.


-- Operador ternário --
Ternário ( ?: ) : Serve para substituir o if-else em casos específicos, utiliza expressões assim como if-else.
```c
```
x == y ? y : z; /* se "x" é igual a "y" então "y", caso não, "z".
x == 200 ? 2 * 5 * 20 : 0; /* se "x" é igual a 200 então 2 * 5 * 20, caso não, 0.


-- Ponteiros --
 Devolvem endereço ou valor na memória do operando, referênciam elementos de uma array (matriz),
modifica os parâmetros das chamadas de função e suporta listas encadeadas e estruturas dinâmicas de dados.

And ( & ): devolve o endereço da memória do operando.
```c
```
int a, b;
b = &a; /* "b" está atribuindo o pointeiro que devolve o endereço da memória de "a".


"Asterisco" ( * ): devolve o valor localizado no endereço de memória do operando.
```c
```
int *a = 10, b;
b = *a; /* váriavel "b" tem seu valor atribuido o pointeiro de "a" que é contém o valor 10.


-- Operador de tamanho --
 Devolve o tamanho ocupado na memória por determinado operando.

sizeof : devolve o tamanho em bytes do operando incluido no parâmetro formal do operador.
```c
```
printf("tamanho de int é: %d bytes\n", sizeof (int)); /* int corresponde a 32 bits ou 4 bytes.


-- Operador de encadeamento --

Virgula ( , ): encadeaia multiplos operandos, no lado esquerdo do operador
será tratado como void, o lado direito torna-se o valor de toda a expressão.
```c
```
int x, y, z; /* define "x" como inteiro, depois "y" e "z".
x = (y = 10, z = 20, y + z); /* "x" tem seu valor atribuido a partir da expressão dentro de parênteses.


-- Operadores de referência --
 Referenciam individualmente os elementos de um struct ou union.

Ponto ( . ): O operador vai referenciar um elemento de um struct ou um union, abaixo um exemplo de um struct.

```c
struct variant { 		/* "variant" é um identificador desse struct. */
	int a;
	char b[9];
} var; 		  			/* "var" é uma váriavel do struct "variant". */
var.a = 120;  			/* váriavel de um struct chamada "var" está referênciando o elemento "a" que tem ser valor atribuido 120. */
```


Seta ( -> ): O operador servirá para referenciar um ponteiro de uma "struct".
```c
```
struct variant *p = &var; /* ponteiro do valor de "p" tem seu valor atribuido ao ponteiro do endereço de "var".
p->abc = 120; /* o ponteiro "p" está atribuindo "abc" o valor 120;


-- Operador de array (matriz) --
 Lista que contém ou não elementos incluidos, todos os elementos são mesmo tamanho e de valor fixo, arrays podem ser mutáveis.

Colchetes ( [] ): O operador realiza a indexação de arrays sobre o operando, onde é possivel aplicar determinada 
quantidade de elementos dentro da array dessa váriavel.

```c
char str[100]; 			/* listamos 100 elementos dentro da array de "str". */
char hi[] = "hello"; 	/* array vazia tem elementos pré-definidos pelo compilador, a array de "hi" tem um "string" atribuido "hello". */
```

-- Operador Cast --

**Cast** 
 O operador cast "(tipo)" forçará determinada expressão a utilizar um tipo especificado entre parênteses. 

```c
#include <stdio.h>
int main(void){
	int i = 1;
	printf("value of i / 2 is %f"(float) i / 2); 	/* float entre parênteses força o número a não ser um inteiro na saída. */
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
|				   |
|				   |
|				   |
|				   |
|				   |
|				   |
