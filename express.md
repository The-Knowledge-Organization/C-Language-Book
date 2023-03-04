# Expressões

## Introdução
 O arquivo atual é exclusivamente sobre as expressões e a estrutura de uma expressão, do que é composta e quais são cada um de seus elementos na linguagem C.

## Expressões
 Expressões são todo o conjunto de tipos, váriaveis, constantes, modificadores, funções e especificadores que juntos formam o que chamamos de expressão, dependendo de sua
funcionalidade a mesma pode ser uma descrição de um calculo a ser efetuado pelo computador, descrever como armazenar na memória determinada palavra em determinado endereço
da memória, descrever uma repetição a ser efetuada para uma verificação e dentre outras coisas, abaixo um exemplo de uma expressão na linguagem C.

```c
void main() {
  static int staticInteger; // Expressão com um modificador de tipo de acesso, do tipo inteiro chamada de "staticInteger"
  return 0;
}
```

## **Tipos básicos**
 Tipos básicos definem como as funções, váriaveis e expressões armazenarão seus valores e como o compilador irá tratar essa váriavel como especificado.

**int**  
 O tipo "int" define a váriavel para armazenar números decimais naturais e caracteres (não é recomendado devido ao tamanho de 4 bytes).

```c
int main() { // Função "main" é do tipo "int", por convenção o código contido dentro do bloco é formado por váriaveis e funções inteiras.

  // Váriavel "number" é do tipo "int", é uma váriavel local que possui um valor atribuido "100"
  int number = 100;
  int character = 'a'; // isso não é uma boa opção pela razão de existir o tipo "char" pra armazenar caracteres
  return 0; // funcão "main()" deve retornar um valor por ser do tipo "int", nesse caso "0" indica sucesso na execução
}
```
___

**char**  
 O tipo "char" define a váriavel para armazenar caracteres e números decimais naturais (com muita limitação devido seu tamanho de 1 byte).

```c
void main() {
  char character = 'a'; // "character" tem atribuido o caractere 'a'
  char maxSignedNumber = 127; // o valor atruibuido "127" é o maximo suportado por padrão
  char minSignedNumber = -128; // o valor atribuido "-128" é o minimo suportado pelo
  char string[5] = "hello"; // matriz "string" contém "5" elementos de mesmo tamanho e tipo onde cada caractere de "hello" ocupa um elemento
}
```

**void**  
 O tipo "void" define a váriavel como nula, sem valor.

```c
void main() { // função "main" com o tipo "void"
  void *pointer; // ponteiro "*" chamado "pointer" é do tipo "void"
}
```

**float**  
 O tipo "float" define a váriavel para armazenar números decimais irracionais e naturais (não recomendado devido a sua precisão de 6 casas decimais após o ponto).

```c
void main() {
  float realNumber = 10.123456;
  float naturalNumber = 1024; // tipo "int" deve ser usado nesse caso
}
```

**double**  
O tipo "double" define a váriavel para suportar o dobro de casas decimais que o tipo "float" (o tamanho de double é de 8 bytes).

```c
void main() {
  double realNumber = 20.2345678910;
  double naturalNumber = 2048;
}
```
___
### **Modificadores de tipos**
 Modificam como cada tipo básico armazena os valores nas váriaveis, os modificadores de tipos se aplicam a int, char, float e double, são
úteis para reduzir os bits de um tipo básico e especificar precisamente o que a váriavel armazenará através do tipo modificado o que economiza
processamento e torna o software mais leve.

**signed**  
 O modificador de tipos "signed" define que os tipos "int" e "char" armazenem números decimais inteiros nas váriaveis (para o compilador os tipos básicos já são "signed).

```c
void main() {
  signed char maxChar = 127; // nesse caso é redudante já que por padrão todos os tipos exceto "void" são "signed". 
  signed char minChar = -128;
}
```

**unsigned**  
 O modificador de tipos "unsigned" define que os tipos "int" e "char" armazenem apenas números decimais naturais nas váriaveis.

```c
void main(){
  unsigned int  = 91;
  unsigned char = 255;
}
```

**long**
 O modificador de tipos "long" define que os tipos "int" e "double" armazenem um valor suportado maior nos valores e bits das váriaveis.

```c
void main(){
  long longInt = 42813; // mesmo tamanho que int
  long int bigInteger = 40531; // int de 64 bits
  long long longerInteger = 31415; // mesmo tamanho que long int
  long double bigFloat = 123.45; // double de 128 bits

}
```

**short**:
 O modificador de tipos "short" define uma modificação que diminui o valor suportado do tipo utilizado e seus bits.

```c
void main() {
  short shortInteger
  short int smallInteger = 10000; // int de 16 bits
}
```

Modificadores permitidos para cada tipo:

|Tipos |Modificadores para cada tipo|
| :-:  |          :-:               |
| int  | signed/unsigned/short/long |
| char |      unsigned/signed       |
|float |           X                |
|double|          long              |


## **Modificadores de tipo de acesso**
 Modificam como as expressões serão covertidas e modificadas pelo compilador.

**const**
 O modificador de acesso "const" define a expressão como apenas-leitura, imutável.

```c
void main() {
  const int rom;
  return 0;
}
```

**volatile**
 O modificador de acesso "volatile" define que a expressão pode ser modificada não explicitamente.

```c
void main() {
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
void main() {
  auto int hello;
  return 0;
}
```

**register**
 O especificador "register" registra a expressão no registrador da C.P.U (que é mais rápido) ou da memória R.A.M (que é mais lento), dependendo do tamanho pode ter um possivel
destaque de desempenho maior em expressões que contém os tipos básicos "int" e "char".

```c
void main() {
  register char str;
  return 0;
}
```

**static**
 O especificador "static" retém o valor entre chamadas de funções quando a expressão tem váriavel local e no caso de expressões com váriaveis globais o seu valor é retido apenas
no arquivo sendo trabalhado.

```c
void main() {
  static int num;
  return 0;
}
```

**extern**
 O especificador "extern" buscará pelo diretório atual a váriavel determinada no código trabalhado.

 Código do arquivo /projetos/**hello.c**

```c
int abc; // váriavel global "abc"

void main() {
  int hi;
  return 0;
}
```

 Código do arquivo /projetos/**hello2.c**

```c
extern abc; // váriavel global "abc" do arquivo "hello.c" utilizada no programa atual trabalhado

void main() {
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
void main() {
  int x, y, z;
  x = y; // atribuição uníca onde "x" tem seu valor atribuido de "y"
  x = y = z; // atribuição multipla onde "x" tem seu valor atribuido de "y" e o mesmo tem o valor atribuido de "z"
  return 0;
}
```

#### **Operadores aritiméticos**
 Os operadores aritiméticos são amplamente utilizados em casos que necessitam de calculos, como no caso de números e expressões que contém multiplos valores, váriaveis ou
expressões, os operadores aritiméticos em sua maioria seguem a "tabela de sinais" utilizada em matemática.

**Adição**
 O operador aritimético de adição "+" especificará o operando como positivo ou efetua calculos de adição.

```c
int main() {
  int a, b, c;
  c = a + b; // Váriavel "a" + "b"
  a = a + b; // Váriavel "a" tem seu valor atribuido "a" + "b"
  a += b; // Forma abreviada da expressão acima
}
```

**Subtração**
 O operador aritimético de subtração "-" especificará o operando como negativo ou efetua calculos de subtração.

```c
void main() {
  int w, x, y, z;
  x = 100;
  y = -x; // Váriavel "y" tem o valor atribuido de "-x" que é "-100"
  z = -y; // Váriavel "z" tem o valor atribuido de "-y" que é "100"
  w = x - z; // Váriavel "w" tem o valor atribuido de "x" subtraido a "z"
  x = x - z;
  x -= z;
}
```

**Multiplicação**
 O operador aritimético de multiplicação "*" serve para efetuar calculos de multiplicação com os operandos.

```c
void main() {
  int x, y, z;
  z = x * y; // Váriavel "z" tem o valor atribuido de "x" * "y"
  x *= y;
}
```

**Divisão**
  O operador aritimético de divisão "/" serve para efetuar calculos de divisão com os operados.

```c
void main() {
  int x, y, z
  z = x / y;
  x /= y;
}
```

**Modulo da divisão**
 O operador aritimético do modulo da divisão "%" serve para mostrar o modulo/resto de um calculo de divisão.

```c
void main() {
  int x, y;
  x % y;
  x %= y;
  return 0
}
```

**Decremento**
 O operador "--" opera sendo binário em expressões, váriaveis, decremento diminui em -1 o valor de determinado operando, e tem uma procedêcia
diferente quando é usado como sufixo ou prefixo do operando.

```c
#include <stdio.h>

void main() {
  int x = 10;
  printf("%d", --x); // subtração de -1 acontece antes, o valor de "x" é 9
  printf("%d", x--); // subtração de -1 acontece depois, o valor de "x" ainda é 9
  printf("%d", x); // o valor atual de "x" é 8
}
```

**Incremento**
  O operador "++" opera sendo binário em expressões, váriaveis, incremento aumenta em +1 o valor de determinado operando, e tem uma procedência
diferente quando é usado como sufixo ou prefixo do operando.

```c
#include <stdio.h>

void main() {
  int y = 5;
  printf("%d", ++y); // O incremento acontece antes. o valor de "y" é 6
  printf("%d", y++); // O incremento acontece depois. o valor de "y" ainda é 6
  printf("%d", y); // O valor atual de "y" é 7
}
```

#### **Operadores relacionais**
 Os operadores relacionais são utilizados em casos que são necessários fazerem alguma relação, comparação entre os operandos definidos e o operador.

**Operador "maior que.."**

```c
void main() {
  x > y; // "x" é maior que "y"
  return 0;
}
```

**Operador "maior que ou igual.."**

```c
void main() {
  x >= y; // "x" maior ou igual a "y"
  return 0;
}
```

**Operador "menor que.."**

```c
void main() {
  x < y; // "x" menor que "y"
  return 0;
}
```

**Operador "menor ou igual.."**

```c
void main() {
  x <= y; // "x" menor ou igual a "y"
  return 0;
}
```

**Operador "igual a.."**

```c
void main() {
  x == y; // "x" igual a "y"
  return 0;
}
```

**Operador "diferente de.."**

```c
void main() {
  x != y; // "x" diferente de "y"
  return 0;
}
```

### **Operadores lógicos**
 Operadores lógicos estabelecem uma lógica específica que determina como os operandos e as expressões se conectarão com os outros.

**And-and ( && )**
 O operador lógico "&&" determina que ambos os operandos devem ter a mesma lógica para ser verdadeiros.

```c
void main() {
  10 != 9 && 20 < 21; // a lógica de âmbos é verdadeira
  10 == 9 && 13 < 22; // a lógica de um é falso e do outro é verdadeiro
  return 0;
}
```

**Or ( || )**
 O operador lógico "||" determina que apenas um dos operandos precisa ser lógico para a expressão ser verdadeira.

```c
void main() {
  int x = 10, y = 1;
  x == y || 20 < 21; // a lógica de um deles é falsa e a outra é verdadeira
  x == y || 20 != 20; // a lógica de um deles é verdadeira e a outra é falsa
  return 0;
}
```

**Not ( ! )**
 O operador lógico not "!" determina que apenas um operando é necessário para operar e pode ser verdadeiro ou falso.

```c
void main() {
  int x = 20, y = 10;
  x != y; // a expressão é verdadeira
  x == !(y + y); // a expresão é falsa
  return 0;
}
```

### **Operadores Bit-a-Bit**
Operadores bit-a-bit servem para atribuir, deslocar bits em bytes ou strings apenas int e char, cada um contém sua "tabela verdade".

**And (&)**
O operador bit-a-bit and "&" desativa o bit de paridade, "and" bit-a-bit é similar ao and lógico.

```c
 1100 0001 // valor de "x" em binário
 0111 1111 // 127 em binário
&
 0100 0001 // "x" sem paridade
```

**Or ( | )**
Ativa os bits com quando é comparado "or" bit-a-bit é similar ao or lógico.

128|3;
```c
 1000 0000 // 128 em binário
 0000 0011 // 3 em binário
|
 1000 0011 // 131 em binário
```


**Or exclusivo (XOR) ( ^ )**
Ativa os bits quando apenas os comparados são diferentes.

127^120;
```c
 0111 1111 // 127 em binário
 0111 1000 // 120 em binário
^
 0000 0111 // 7 em binário
```

**Complemento de um ( ~ )**
Inverte o estado atual dos bits.
```c
 1110 0110 // byte original
 0001 1001 // após o primeiro complemento
 1110 0110 // após o segundo complemento
```

**Deslocamento a esquerda ( << )**
Deslocará bits para a esquerda e adicionarará zeros aos da direita.

```c
// "y" tem seu valor atribuido a 7 e se deslocará apenas 1 bit a esquerda.
x = y<<1;

0000 0111 // 7 em binário e antes da deslocação
0000 1110 // 14 em binário e após a deslocação
```

**Deslocamento a direita ( >> )**
Deslocará bits para a direita e adicionarará zeros aos da esquerda.
```c
/* "y" tem seu valor atribuido a 14 e se deslocará apenas 1 bit a direita */
x = y>>1;

0000 1110 // 14 em binário e antes da deslocação
0000 0111 // 7 em binário e após a deslocação
```

### Operador ternário(:?)

Serve para substituir o if-else em casos específicos, utiliza expressões assim como if-else.

```c
// Se "x" é igual a "y" então "y", caso não, "z"
x == y ? y : z;

// Se "x" é igual a 200, então 2 * 5 * 20 caso contrário, 0
int result = x == 200 ? 2 * 5 * 20 : 0;
```

### **Ponteiros**
Devolvem endereço ou valor na memória do operando, referênciam elementos de uma array (matriz), modifica os parâmetros das chamadas de função e suporta listas encadeadas e estruturas dinâmicas de dados.

**And ( & )**
Devolve o endereço da memória do operando.

```c
int a, b;

// "b" está atribuindo o pointeiro que devolve o endereço da memória de "a"
b = &a;
```

**"Asterisco" ( * )**
Devolve o valor localizado no endereço de memória do operando.

```c
int *a = 10, b;

// Váriavel "b" tem seu valor atribuido o pointeiro de "a" que é contém o valor 10
b = *a;
```

### **Operador de tamanho**

Devolve o tamanho ocupado na memória por determinado operando.

**sizeof**
Devolve o tamanho em bytes do operando especificado a frente ou incluido no parâmetro do operador se houver uma expressão.

```c
// int corresponde a 32 bits ou 4 bytes
printf("tamanho de int é: %d bytes\n", sizeof int);
```

### Operador de encadeamento

**Virgula ( , )**
 Encadeaia multiplos operandos, no lado esquerdo do operador
será tratado como void, o lado direito torna-se o valor de toda a expressão.

```c
int x, y, z; // Define "x" como inteiro, depois "y" e "z"
x = (y = 10, z = 20, y + z); // "x" tem seu valor atribuido a partir da expressão dentro de parênteses
```

### Operadores de referência
Referenciam individualmente os elementos de um struct ou union.

**Ponto ( . )**
O operador vai referenciar um elemento de um struct ou um union, abaixo um exemplo de um struct.

```c
// "variant" é um identificador desse struct
struct variant{
  int a;
  char b[9];
} var; // "var" é uma váriavel do struct "variant"

// Váriavel de um struct chamada "var" está referênciando o elemento "a" que tem ser valor atribuido 120
var.a = 120;
```

**Seta ( -> )**
O operador servirá para referenciar um ponteiro de uma "struct".

```c
// Ponteiro do valor de "p" tem seu valor atribuido  ao ponteiro do endereço de "var"
struct variant *p = &var;

// O ponteiro "p" está atribuindo "abc" o valor 120
p->abc = 120;
```

### Operador de array (matriz)
Lista que contém ou não elementos incluidos, todos os elementos são mesmo tamanho e de valor fixo, arrays podem ser mutáveis.

**Colchetes ( [] )**
O operador realiza a indexação de arrays sobre o operando, onde é possivel aplicar determinada quantidade de elementos dentro da array dessa váriavel.

```c
char str[100]; // listamos 100 elementos dentro da array de "str"

// os elementos aqui serão pré-definidos pelo compilador onde a array "hi" contém armazenado em cada elemento um caractere de "hello"
char hi[] = "hello";

// é recomendável que se especifique exatamente quantos elementos vão ser necessários quando passar uma string
char hi[6] = "hello";
```

### Operador Cast

**Cast**
O operador cast "(tipo)" forçará determinada expressão a utilizar um tipo especificado entre parênteses.

```c
#include <stdio.h>
void main() {
  int i = 1;

  // "float" entre parênteses força o número a não ser um inteiro na saída
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
