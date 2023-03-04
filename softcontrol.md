# Controle de software

## Introdução
 Este é um dicionário razoávelmente informativo sobre a linguagem C do padrão da American National Standards Institute (ANSI), o arquivo atual é
exclusivamente sobre os comandos de controle de software.

___

## Comandos de controle do software
 Controle do software é necessário nas linguagens de programação para determinar ações especificas no software, são responsáveis por fazer seu código executar trechos
especificos, ou expressões especificas onde você controla como, onde e quando uma ação acontecer.

### Comandos condicionais
 Condicionais são conhecidas por dependerem de uma ação especificada pra acontecer ou seja, é necessário  que uma condição esteja correta pra ser executada a instrução.

**if-else**
 A condição "if-else" determina que, se o argumento no parâmetro formal de "if" é verdadeiro acontece uma ação logo em sequência, seja dentro de um bloco ou não,
caso não  o "else" é executado, a utilização de else é opcional e if-else pode ser colocado dentro do outro if-else.

```c
#include <stdio.h>

int main(void) {
	int x;

	printf("put a number: ");
	scanf("%d", &x);

	if(x < 10) printf("lower than 10\n");
	else printf("higher than 10\n");

	return 0;
}
```

 Outro exemplo de utilizaão do "if-else" nesse caso o código é com o objetivo de criar um jogo de advinhação:

```c
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	int gss;
	int rdm = rand(); // função da biblioteca "stdlib.h", nessa função obtem-se o número máximo suportado de um determinado tipo usado.

	printf("Guess the number: ");
	scanf("%d", &gss);

	if(rdm == gss) {
	    printf("Nice! the number I selected was %d, and your answer is: %d\n ", rdm, gss);
        printf("this is the maximum number supported by the 32 bits 'int' type.");
	} else printf("You've missed!, the number I thought was %d \n", rdm);

	return 0;
}
```
___

**switch-case-default**
 A condição "switch-case-default" testa o valor da expressão aplicado no parâmetro formal de "switch" contra as constantes aplicadas aos "cases", quando o valor da expressão
coincide com a constante a mesma é executada, "default" é opcional, switch-case-default pode ser colocado dentro de outro switch-case-default.
 Abaixo tem um exemplo de um programa de calculo usando "switch-case-default".

```c
#include <stdio.h>

int main() {
    int n0, n1, res;
    char op0;

    printf("Insira o primeiro número: ");
    scanf("%d", &n0);

    printf("Adição (+)\n\n");
    printf("Subtração (-)\n\n");
    printf("Multiplicação (*)\n\n");
    printf("Divisão (/)\n\n");

    printf("Use um dos operadoradores: ");
    scanf(" %c", &op0);

    printf("Segundo número: ");
    scanf(" %d", &n1);

    switch(op0) {
        case '+': res = n0 + n1; break;
        case '-': res = n0 - n1; break;
        case '*': res = n0 * n1; break;
        case '/': res = n0 / n1; break;
        default: printf("Erro!");
        }

    printf("Resultado: %d %c %d = %d\n", n0, op0, n1, res);
    return 0;
}
```
___
### Comandos de laço
 Comandos de laço ou loop, são conhecidos por repetirem uma ação determinadas quantidades de vezes, onde o programador pode escolher onde, quando
e em que trecho do código repetir o trecho de tal código.

**for**
 O comando de loop "for" analisará se determinada expressão aplicada ao inicio do parâmetro formal é verdadeira, caso não, o resto do parâmetro da função "for" não é
executado, cada expressão é separada por ";" (ponto e virgula), indicando o fim da expressão e após isso o inicio de outra expressão.

 Exemplo de loop:

```c
#include <stdio.h>

int main(void) {
	int x;
    // No parâmetro formal váriavel "x" tem valor "1" atribuido, se "x" ser menor que "100", incrementa o valor de "x" em +1.
    for(x = 1; x < 100; x++) {
	    printf("value of x is: %d \n", x); // "printf" se repete 100 vezes imprimindo o que está no parâmetro de e o valor de 1 até 100.
    }
    return 0;
}
```

 E aqui também:

 ```c
#include <stdio.h>

int main(void) {
	int x;
    for(x = 1; x < 100; x++) printf("value of x is: %d \n", x); // identação recomendada por apenas conter uma unica função
    return 0;
}
```

 Aqui já não temos um loop:

```c
#include <stdio.h>

int main(void) {
	int x;
    for(x = 1; x < 100; x++); /* devido ao ponto e virgula "for" não irá prosseguir com o loop */
	printf("value of x is: %d \n", x); /* "printf" não repete o valor "100" */
    return 0;
}
```
