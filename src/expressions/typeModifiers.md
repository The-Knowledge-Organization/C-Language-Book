### **Modificadores de tipos** 
 Modificam a maneira como cada tipo básico define as váriaveis, os modificadores se aplicam apenas aos tipos ...

**signed**  
 O modificador de tipos "signed" define que os tipos sejam modificados para suportar números positivos e negativos entre -127 até +128.

```c
int main(void){
	signed int x = -10;
	signed int y = 20;
	return 0;
}
```

**unsigned**  
 O modificador de tipos "unsigned" define que os tipos sejam modificados para suportar apenas números positivos de 0 até 255.

```c
int main(void){
	unsigned int y = 91;
	return 0;
}
```

**long**  
 O modificador de tipos "long" define uma modificação que aumenta o valor suportado do tipo utilizado e seus bits.

```c
int main(void){
	long int z = 100; 				/* int de 64 bits. */
	long double numf = 123.45; 		/* double de 128 bits. */
	return 0;
}
```

**short**  
 O modificador de tipos "short" define uma modificação que diminui o valor suportado do tipo utilizado e seus bits.

```c
int main(void){
	short int z = 10000;	/* int de 16 bits. */
	return 0;
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
