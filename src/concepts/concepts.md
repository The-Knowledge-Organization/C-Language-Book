## Conceitos básicos

- ### Linguagem C
 A linguagem de programação C foi publicamente lançada em 1972, desenvolvida entre 1969-1972 nos laboratórios da Bell Labs (na época da empresa AT&T e 
atualmente é um setor da Nokia) por Dennis Ritchie (1941 - 2011) para o sistema operacional Unix, a linguagem de programação C é procedural, fortemente tipada
de propósito geral e turing complete.

- ### Estrutura da linguagem C
 Um código em C contém uma estrutura similar a esta abaixo descrita onde o código está indentado e descrito em português para melhor compreensão para quem não
tem nenhuma noção, de como um código em C é construido. 

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
 
 Na linguagem C essa é a sintaxe encontrada:

```c
#include <stdio.h>	/* 	Comando para o pré-processador "#include" se substitui pelo conteúdo do arquivo que se localiza no diretório
						padrão do compilador indicado por "< >" que contém o arquivo com o nome de "stdio.h" */   
					 
int a;	/* Váriavel global inteira "a". */

int main(void){    /* Função "main" tem o paramêtro formal "()" do tipo "void" e um bloco de código "{}" para a adição das linhas de código. */
					
	char str[0];    /* Váriavel do tipo "char" chamada "str" contém um elemento "0" dentro do operador de array "[]". */

	printf("input a string: ");		/* Função "printf()" do arquivo "stdio.h" serve para imprimir o que foi colocado no parâmetro formal. */
	scanf("%s", str);	/* Função "scanf()" do arquivo "stdio.h" serve para coletar a entrada de um valor "%s" que nesse caso é string "str". */

	printf("input a num: ");
	scanf("%d", &a);	/* "%d" aceita exclusivamente digitos (1, 2, 3). */

	printf("the string you put is '%s' and the num is '%d'\n", str, a);

	return 0;	/* "return" está retornando nesse caso um valor inteiro "0" devido a função "main" ser do tipo "int". */
}

```


