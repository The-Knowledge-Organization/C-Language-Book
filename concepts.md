# Dicionário da linguagem de programação C  

## Introdução  
 
 Este é um dicionário razoávelmente informativo sobre a linguagem C do padrão da American National Standards Institute (ANSI), o arquivo atual é exclusivamente sobre seus 
conceitos e termos aplicados não só exclusivamente a essa linguagem mas a toda programação e tecnologia.
___

## Conceitos

- ### Linguagem C
 A linguagem de programação C foi publicamente lançada em 1972, desenvolvida entre 1969-1972 nos laboratórios da Bell Labs (na época da empresa AT&T e atualmente é 
um setor da Nokia) por Dennis Ritchie (1941 - 2011) para o sistema operacional Unix, a linguagem de programação C é procedural, fortemente tipada, de propósito geral e turing
complete.

- ### Estrutura da linguagem C
 Um código em C contém uma estrutura similar a esta abaixo descrita onde o código está indentado e descrito em português para melhor compreensão para quem não tem nenhuma noção, 
de como um código em C é construido. 

```
pré-processador inclusão <biblioteca padrão de I/O>

tipo váriavel;
modificador tipo váriavel;

tipo-inteiro função(){
	tipo váriavel = 'y';
	modificador tipo váriavel = 100;
	tipo função();
	retorno número-inteiro;
}
```
 
 Na linguagem C essa é a sintaxe encontrada:

```c
#include <stdio.h>	/* 	Comando para o pré-processador "#include" se substitui pelo conteúdo do arquivo que se localiza no diretório
						padrão do compilador indicado por "< >" que dentro contém o arquivo definido com o nome de "stdio.h" */   
					 
int a;	/* Váriavel global inteira "a". */

int main(void){	 /* Função "main" tem o seu paramêtro formal "()" do tipo "void" e contém um bloco de código "{}" por conta da inclusão de várias linhas de código. */
					
	char str[0];	/* Váriavel do tipo "char" chamada "str" contém um elemento "0" dentro de sua array "[]". */

	printf("input a string: ");		/* Função "printf()" da biblioteca "stdio.h" serve para imprimir a atribuição do parâmetro formal. */
	scanf("%s", str);	/* Função "scanf()" da biblioteca "stdio.h" serve para coletar a entrada de um valor que é string "%s" e logo após a váriavel "str". */

	printf("input a num: ");
	scanf("%d", &a);	/* "%d" aceita exclusivamente digitos (1, 2, 3). */

	printf("the string you put is '%s' and the num is '%d'\n", str, a);

	return 0;	/* O comando "return" está retornando um valor inteiro "0" devido a função "main" ser do tipo "int". */
}

```

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

___

- ### Tempo de compilação 

___

- ### Tempo de execução

___

- ### Mapa de memória  
 O mapa de memória mostra como o programa fica organizado na memória após o processo de compilação e linkedição, no caso da linguagem C e do compilador GCC ficará dessa forma.  

|	   Partes		|											Definições													 |
|		:-:			| 												-														 |
| 	Stack (Pilha) 	|  Contém variaveis locais, o retorno de chamadas de funções, argumentos das funções e o estado da CPU.  |
|	 Heap (Monte)	|			Memória livre que serve para ser alocada com as funções de alocamento de memória.			 |
| Váriaveis globais |      Váriaveis que estão fora de um bloco de código e que estarão disponiveis por todo o código.  	 |
|   Código fonte	|	 Conjunto de todas as "instruções" escritas em determinada linguagem nesse caso a linguagem C. 		 |    

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
declaração.


- ### Fracamente tipada
 Linguages de programação fracamente tipadas são conhecidas por não utilizarem tipos para definição das váriaveis que estão presente no código.
___

- ### Dinâmicamente tipada
 Linguagens de programação dinamicamente tipadas
