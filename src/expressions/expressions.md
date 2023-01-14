## **Expressões** 
 Expressões são quando temos um conjunto de tipos, váriaveis, constantes, modificadores, funções e especificadores que juntos formam o que chamamos de expressão. 

```c
int main(void){
	static int stc;		/* Expressão com um modificador de tipo de acesso, do tipo inteiro chamada de "stc". */
	return 0;
}
```

## **Tipos básicos**
 Tipos básicos servem para definirem como as funções, váriaveis, paramêtros formais e expressões serão lidas para o compilador.
___

**int**  
 O tipo "int" define a váriavel pra aceitar especificamente os caracteres inteiros.

```c
int fn; 				/* Váriavel global "fn" é do tipo "int". */
int main(void){ 		/* Função "main" é do tipo "int", essa função executa todo o programa. */
	int fun = 100; 		/* Váriavel "fun" é do tipo "int", é uma váriavel local que possui um valor atribuido "100". */
	return 0;
}
```

**char**  
 O tipo "char" define a váriavel pra aceitar especificamente caracteres.

```c
int main(void){
	char str = 'i';		/* Váriavel "char str" tem atribuido o caractere 'i'. */
	char num = 100;		/* Variavel "char num" tem o valor atruibuido 100. */
}
```

**void**  
 O tipo "void" define a váriavel como nula, vazia, sem valor.

```c
int main(void){		/* função "main" contém no seu parâmetro o tipo "void". */	
	void *p1;		/* váriavel de ponteiro "*p1" é do tipo "void". */
	return 0;
}
```

**float**  
 O tipo "float" define a váriavel pra aceitar os números com precisão ou seja ponto flutuante.

```c
int main(void){
	float fnum = 10.123;
	return 0;
}
```

**double**  
O tipo "double" suporta o dobro de casas decimais que o tipo "float".

```c
int main(void){
	double dnum = 20.123;
	return 0;
}
```

**Tabela de bits dos tipos básicos**  
 A tabela abaixo utiliza o operador "sizeof" que mede o tamanho em bytes de seu operando dentro de seu parâmetro formal.

|  Tipos  |   Bits   |	 Bytes	|
|  :--	  |    --    |	  --:	|
|  void	  |	   08    |	  01	|
|  char   |	   08    |	  01	|
|  int    |    32    |	  04	|
|  float  |    32    |	  04	|
| double  |    64    |	  08	|




