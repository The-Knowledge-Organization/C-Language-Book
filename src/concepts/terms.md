## Termos

- ### Código Fonte  
 Quando escrevemos em um arquivo usando uma determinada linguagem de programação isso se torna o código uma descrição simplificada para o programador redirecionar ao tradutor que 
pode ser o interpretador ou compilador e que traduzirá tudo o que foi escrito para a linguagem da "maquina", que nesse caso é o código binário, quando você faz algum "software" 
essas descrições se tornam o código fonte de determinada aplicação a qual está sendo criada e que foi feita em uma linguagem especifica.
___

- ### Assembler
  

___

- ### Linkeditor  
 O linkeditor vai unir o código escrito na linguagem de base e compilada para a linguagem alvo, nesse caso o código em C é transformado em Assembly pelo assembler, onde 
todo o código base foi reescrito para assembly, nisso o linkeditor pegará todas as intruções do seu código e irá buscar pelas bibliotecas incluidas, expressões e unirá isso 
tudo em um único arquivo que é chamado de "código objeto".
___

- ### Código Objeto  
 Após o processo de compilação você tem o que se chama de código binário nesse caso código objeto, é esse o código que você obtem quando ocorre com sucesso o processo de 
compilação e linkedição você tem o código objeto, onde há todas as instruções para ser executado na arquitetura e sistema operacional da máquina atual ou na máquina onde deseja 
executar esse código, isso tudo dependerá do compilador utilizado e a versão da linguagem C.
___

- ### Arquivo de cabeçalho
 Os arquuivos de cabeçalho conhecidos como "header" são arquivos onde por convenção incluirá bibliotecas, comandos para o pré-processador, funções e dentre outras coisas 
que você necessitará ao longo do projeto para serem utilizados pelo seu arquivo de onde está o código fonte.
___

- ### Tempo de compilação 

___

- ### Tempo de execução

___

- ### Mapa de memória  
 O mapa de memória demonstra como o programa fica organizado na memória (R.A.M) após o processo de compilação e linkedição, na linguagem C com compilador GCC ficará dessa forma.

|	   Partes		|											Definições													|
|		:-:			| 												-														|
| 	Stack (Pilha) 	| Contém variaveis locais, o retorno de chamadas de funções, argumentos das funções e o estado da CPU.  |
|	 Heap (Monte)	| Memória livre que serve para ser alocada com as funções de alocamento de memória.		                |
| Váriaveis globais | Váriaveis que estão fora de um bloco de código "{}" e se fazem presente pelo  código.                 |
|   Código fonte	| Conjunto de todas as "instruções" escritas em determinada linguagem nesse caso a linguagem C. 		|    

___

- ### Interpretador e compilador

___

- ### Programação procedural

___

- ### Programação orientada a objetos

___

- ### Programação funcional

___

- ### Turing complete

___

- ### Fortemente tipada
 Linguagens de programação fortemente tipadas são conhecidas por utilizarem os seus tipos para o código funcionar, então o compilador/interpretador já sabe como 
deverá tratar determinada váriavel porquê o tipo está especificando-a.
 ___

- ### Estaticamente tipada
 Linguagens de programação estaticamente tipadas são conhecidas por manterem seu tipo e normalmente especificarem explicitamente o tipo utilizado em determinada váriavel na sua 
declaração e C é uma linguagem estaticamente tipada, como é possivel ver no exemplo abaixo.

```c
int integer = 10;
char character = 'y';
char str[] = "Hello!";
float piNum = 3.1415;
double goldNum = 1.618;
void *null;
```

- ### Fracamente tipada
 Linguages de programação fracamente tipadas são conhecidas por não utilizarem tipos para a definição das váriaveis que estão presente no código. No caso da linguagem C,
isso não aconteceria devido a como foi contruida, obrigatóriamente utilizando tipos, mas com muito esforço é possivel tornar C uma linguagem fracamente tipada.
___

- ### Dinâmicamente tipada
 Linguagens de programação dinamicamente tipadas podem ter a especificação ou não de seus tipos, nisso é possivel a intercalação entre definir ou não
uma váriavel ou deixar o compilador/interpretador fazer isso "automáticamente", no caso de C isso é possivel também, mas lembre-se que isso não
é algo que a linguagem foi projetada para suportar.
