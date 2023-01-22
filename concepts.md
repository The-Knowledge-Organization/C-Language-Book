# Dicionário da linguagem de programação C  
 
## Introdução  
 Este dicionário reune todas as informações sobre a linguagem de programação C do padrão da American National Standards Institute (ANSI), 
o arquivo atual é exclusivamente sobre os conceitos e termos do mundo da programação e da tecnologia aplicados a essa linguagem.  
___

## Termos e conceitos

- ### Linguagem C
  A linguagem de programação C foi lançada ao público no ano de 1972, desenvolvida entre os anos de 1969 até 1972 nos laboratórios da Bell Labs 
(na época da empresa AT&T e atualmente é um setor da empresa Nokia) inicialmente por Dennis Ritchie (1941 - 2011) para o sistema operacional Unix, 
a linguagem de programação C é procedural, estaticamente tipada, de propósito geral e turing complete.

  Um código em C contém uma estrutura similar a esta abaixo,  onde o código está indentado e descrito em linguagem natural (PT-BR) para melhor
compreensão para quem não tem nenhuma noção ou conhecimento de como um trecho de código ou software é escrito na linguagem C. 

```
pré-processador inclusão <biblioteca padrão de I/O>

tipo váriavel;
modificador tipo váriavel;

tipoInteiro função(){
	tipo váriavel = 'y';
	modificador tipo váriavel = 100;
	tipo função();
	retorno número-inteiro;
}
```
 
 A linguagem C contém esta sintaxe abaixo:

```c
#include <stdio.h> /* Comando para o pré-processador "#include" se substitui pelo conteúdo do arquivo que se localiza no diretório
						padrão do compilador indicado por "< >" que contém o arquivo com o nome de "stdio.h" */   
					 
int a;	/* Váriavel global do tipo int "a". */

int main(void){ /* Função "main" tem o paramêtro formal "()" do tipo "void" e um bloco de código "{}" para a adição das linhas de código. */
					
    char str[0]; /* Váriavel do tipo "char" chamada "str" contém um elemento "0" dentro do operador de array "[]". */

    printf("input a string: "); /* Função "printf()" do arquivo "stdio.h" serve para imprimir o que foi colocado no parâmetro formal. */
    scanf("%s", str); /* Função "scanf()" do arquivo "stdio.h" serve para coletar a entrada de um valor "%s" que nesse caso é string "str". */

    printf("input a num: ");
    scanf("%d", &a); /* "%d" aceita exclusivamente digitos (1, 2, 3). */

    printf("the string you put is '%s' and the num is '%d'\n", str, a);

    return 0; /* "return" está retornando nesse caso um valor inteiro "0" devido a função "main" ser do tipo "int". */
}
```
___

- ### Código Fonte  
  Quando um software é escrito seja em um ou mais arquivos usando uma determinada linguagem é com o objetivo de descrever de forma simplificada
para o programador entender o que esse código faz e qual é o seu objetivo e então ordenar a maquina através desse código ao que deve fazer,
isso é o que se chama de código fonte, onde o software fica armazenado junto com todas as suas instruções, bibliotecas, imagens e arquivos 
para fazer com que se execute de maneira funcional e eficiente. 
___

- ### Assembler
  O assembler é uma ferramenta incluida no compilador que serve para reescrever o código escrito na linguagem de base para a linguagem alvo,
nesse caso o código em C é transformado em Assembly na etapa inicial do processo de compilação. 
___

- ### Linkeditor  
  O linkeditor une o código C reescrito em Assembly pelo "assembler" e irá buscar pelas bibliotecas incluidas, expressões, funções e unirá 
isso tudo em um único arquivo que é chamado de "código objeto" e que pode variar de arquitetura, sistema operacional e hardware usados no 
processo de compilação assim gerando um binário específico pra a máquina base ou alvo.
___

- ### Código Objeto  
  Após o processo de compilação você tem o que se chama de código binário ou código objeto, esse é o código que você obtem quando ocorre 
com sucesso o processo de compilação e linkedição onde há todas as instruções para ser executado na arquitetura e sistema operacional da 
máquina atual ou na máquina alvo, todo o processo dependerá do compilador/interpretador utilizado e qual é a versão da linguagem C sendo usada.
___

- ### Arquivo de cabeçalho 
  Os arquivos de cabeçalho conhecidos como "header" são arquivos onde por convenção incluirá bibliotecas, comandos para o pré-processador,
funções e o que você necessitará ao longo do projeto para serem utilizados pelo código do software.
___

- ### Tempo de compilação 
  O termo "tempo de compilação" são uma junção de eventos que acontecem em processo de compilação e que não ocorrem na execução, são processos
feitos inteiramente pelo compilador um exemplo desses processos é o de compilação, assembler e a linkedição.
___

- ### Tempo de execução
  O termo "tempo de execução" contém eventos que acontecem no processo de execução de determinado software ou código e de tudo que foi 
incluido no código fonte como bibliotecas, funções, váriaveis, estruturas.
___

- ### Mapa de memória  
    O mapa de memória demonstra como o programa fica organizado na memória (R.A.M) após o processo de compilação e linkedição, na 
linguagem C com compilador GCC ficará dessa forma.

|	   Partes		|											Definições													|
|		:-:			| 												:-:														|
| 	Stack (Pilha) 	| Contém variaveis locais, o retorno de chamadas de funções, argumentos das funções e o estado da CPU.  |
|	 Heap (Monte)	| Memória livre que serve para ser alocada com as funções de alocamento de memória.		                |
| Váriaveis globais | Váriaveis que estão fora de um bloco de código "{}" e se fazem presente pelo  código.                 |
|   Código fonte	| Conjunto de todas as "instruções" escritas em determinada linguagem nesse caso a linguagem C. 		|    

___

- ### Interpretador e compilador
  Interpretadores e compiladores existem na maioria das linguagens de programação, seja de scripting, funcional, procedural, orientada a
objetos e dentre outras, a maneira como o interpretador funciona é com a leitura sendo linha por linha do código, eliminando as dependencias
que o código precisa seja bibliotecas, funções e entrega a execução de todo o programa na saída do terminal, no caso do compilador há um 
processo que pode ser lento em casos específicos, mas no final entrega um desempenho absurdo em comparação com o interpretador.  
 
  Em resumo o interpretador tem sua execução mais lenta mas o código sai mais rápido e não gera o código objeto e o compilador é mais lento
devido ao processo de compilação mas entrega uma execução infinitamente mais rápida e gera o código objeto. Em C existe a possibilidade de 
se criar um interpretador usando a própria linguagem e de maneira bem eficiente.
___

- ### Programação procedural
  A maioria das linguagens de programação atualmente são procedurais como C++, Rust e no caso a linguagem C é procedural também ou seja,
dependerá que o código escrito seja organizado e estruturado para funcionar da maneira que for desejada, aqui um trecho que demonstra bem 
esse conceito de programação procedural: 

```c
#include <stdio.h>

void fun(void){  /* Função "fun()" contém o código necessário pra armazenar uma string */
    char str[] = "Hello \n"; /* Aqui armazenamos na array de str a string "Hello \n" */
    printf("%s", str); /* Imprime na saida o valor armazenado da array de str */
}

int main(void){
    fun(); /* Aqui a função "fun()" será executada primeira do que a função "printf()" */
    printf("Goodbye");
    return 0;
}
```
___

- ### Programação orientada a objetos

___

- ### Programação funcional

___

- ### Turing complete
   O termo "turing complete" foi criado em homenagem ao cientista da computação [Alan Turing](https://en.wikipedia.org/wiki/Alan_Turing)
para descrever a capacidade que uma "máquina de turing" teria de se simular, ou seja a máquina é capaz de reconhecer ou decidir como definir
as regras de manipulação de dados assim possibilitando que uma maquina "A" simule uma maquina "B" e vice-versa, hoje em dia a maior parte das
linguagens de programação são "turing complete" como por exemplo a linguagem C onde é possivel a criação de uma linguagem baseada na mesma,
linguagens como Python, Lua, C++ utilizaram C para serem criadas.
___

- ### Estaticamente ou fortemente tipada
  Linguagens de programação estaticamente/fortemente tipadas são conhecidas por obrigarem a especificação de maneira explicita do tipo
utilizado nas váriaveis na sua declaração, C é uma linguagem que foi projetada com esse intuito de ser estaticamente/fortemente tipada, como 
é possivel ver no exemplo abaixo:

```c
int integer = 10;
char character = 'y';
char str[] = "Hello!";
float piNum = 3.1415;
double goldNum = 1.618;
void *null;
```
___

- ### Dinâmicamente ou fracamente tipada
  Linguages de programação dinâmicamente/fracamente tipadas são conhecidas por não obrigarem a utilização dos tipos para a definição das 
váriaveis que estão presente no código nisso é possivel a intercalação entre definir o tipo ou não de uma váriavel ou deixar o compilador ou
interpretador fazer isso "automáticamente". 
  
  No caso da linguagem C, isso não aconteceria devido a como foi contruida, mas com muito esforço é possivel tornar C uma linguagem 
dinâmicamente/fracamente tipada mas lembre-se que isso não é algo que a linguagem foi projetada para suportar.
___

- ### Sistema binário

  O sistema binário ou sistema de base dois é uma das formas mais básicas para se representar dados sendo o valor positivo representado "0" e 
negativo por "1", usando uma sequência de 8 bits podemos representar dados com "bytes" que significa **b**inar**y** **te**rms, "termos binários"
são utilizados para armazenar informações nisso podemos representar números de base decimal, octal, hexadecimal e dentre outros e assim 
aumentando a ordem de grandeza tem os kilobytes, megabytes, gigabytes, terabytes e assim por diante
 
  Para representarmos por exemplo o número decimais em sistema binário é dessa forma abaixo:

  |  Decimal   |  Binário   |
  |    :-:     |     :-:    | 
  |    10      |  0000 1010 | 
  |     9      |  0000 1001 |
  |     8      |  0000 1000 |
  |     7      |  0000 0111 |
  |     6      |  0000 0110 |
  |     5      |  0000 0101 |
  |     4      |  0000 0100 |
  |     3      |  0000 0011 |
  |     2      |  0000 0010 |
  |     1      |  0000 0001 |
 
  Se adicionarmos 1 bit a mais no byte que corresponde ao valor 8 na tabela iremos para 9, o máximo que 1 byte suporta é o número decimal 255
após isso para representar o número 256 é dessa forma "1111 1111 1", se utilizassemos o número decimal máximo de 2 bytes (16 bits) teremos 
o número 65536.

- ### Tabela de bits/bytes

 A tabela abaixo mostra o tamanho em bits e bytes dos tipos básicos.

|  Tipos  |   Bits   |	 Bytes	|
|  :---:  |   :---:  |	 :---:	|
|  void	  |	   08    |	  01	|
|  char   |	   08    |	  01	|
|  int    |    32    |	  04	|
|  float  |    32    |	  04	|
| double  |    64    |	  08	|


___
- ### Tamanho dos tipos em C
  
  Em C é possivel saber exatamente qual é o tamanho máximo suportado por cada tipo, modificador de tipos, modificadores de tipo de acesso
usando um arquivo header chamado "limits.h" e "float.h" para ter acesso aos tipos float e double, nesses "headers" contém váriaveis onde é 
possivel saber o quanto um tipo pode suportar de válor minímo e máximo em números de base decimal, abaixo uma demonstração em códifgo de como 
quanto cada tipo suporta, desde seu valor minimo até seu valor máximo:

```c
#include <stdio.h>
#include <limits.h>
#include <float.h>

int main(void){
    int intMax = INT_MAX, intMin = INT_MIN;
    char charMax = CHAR_MAX, charMin = CHAR_MIN;
    float floatMax = FLT_MAX, floatMin = FLT_MIN;
    double doubleMax = DBL_MAX, doubleMin = DBL_MIN; 
    int ans;

    printf("Type size verifier.\n"
           "Select the type you want: \n\n"
           "int max(1)\n"
           "int min(2)\n"
           "char max(3)\n"
           "char min(4)\n"
           "float max(5)\n"
           "float min(6)\n"
           "double max(7)\n"
           "double min(8)\n");
    scanf("%d", &ans);

    switch(ans){
        case 1: printf("the maximum number supported by int is: %d", intMax); break;
        case 2: printf("the minimum number supported by int is: %d", intMin); break;
        case 3: printf("the maximum number supported by char is: %d", charMax); break;
        case 4: printf("the minimum number supported by char is: %d", charMin); break;
        case 5: printf("the maximum number supported by float is: %f", floatMax); break;
        case 6: printf("the minimum number supported by float is: %f", floatMin); break;
        case 7: printf("the maximum number supported by double is: %f", doubleMax); break;
        case 8: printf("the minimum number supported by double is: %f", doubleMin); break;
        default: printf("Error");
    }

    return 0;
}
```
