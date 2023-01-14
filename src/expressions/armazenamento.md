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
