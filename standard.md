# Instruções para o dicionário

 Se caso optou por ajudar o projeto a ganhar mais conteúdo é necessário seguir o padrão definido para que tenha uma melhor compreesão e entendimento
para o leitor e editor sobre os conteúdos abordados em cada texto de cada cápitulo dos dicionários, iremos começar com a sintaxe do código
inserido nos exemplos, lembre-se de que você programa para outros programadores entenderem seu código e poderem lhe ajudar, o compilador/interpretador vai
alterar **tudo** o que você fez e escreverá do jeito mais eficiênte possível para sua máquina e sistema operacional atual ou alvo.

 Um trecho de uma linguagem de programação nos dicionários deve conter a seguinte identação:

```c
#include <stdio.h>

/* Comentários longos acima do bloco código e de preferência que abrange a maior compatibilidade entre versões e performance
   como por exemplo o comentário de muliplas linhas da linguagem C */
int main(void) {
  int number; // comentários menores ao lado do código e váriaveis com nomes que explicitem sua função
  char string[24] = "the value of num is now\0"; // espaço de uma linha para dar o inicio a uma nova parte do código

  // é necessário fazer com que as funções sejam legiveis como esta abaixo
  for(number = 0; number < 100; number++) printf("the value of num is: %d\n", number);

  printf("%s %d", string, number);
  return 0;
}
```

 Em textos, lembre-se de que sempre que escreve algo, leia o que escreveu, interprete a sua explicação, procure não repetir palavras, girias
ou até mesmo acrônimos com frequência para não tornar a experiência do leitor entediante, quando explicar algo seja direto ao ponto,
sem tângentes que vão muito além do assunto principal, aspas duplas para termos, expressões, acrônimos e o que for relacionado a linguagem
como "assembly", "machine learning", "software", "ram" e assim por diante, um exemplo de tudo isso que mencionei seria isso:

```
 "Nesse trecho temos um código que faz o seguinte, esse código tem um algoritimo, que é uma junção de for e loops que fazem a repetição
 acontecer e no código o algoritimo é o que faz repetir o número 100 vezes..."
```

 Não está impossível de se entender mas tem como fazer melhor:

```
 "No código contém um "algoritimo" (que é uma junção de váriaveis, funções de laço...) que repetirá o número 100 vezes... "
```

 A explicação foi encurtada e ainda há uma compreensão do que se trata, e como pode ver acima quando explicar um termo coloque entre
parênteses, não é necessário se estender já que os existe o arquivo de "termos e conceitos" para exclarecer melhor o que de fato serve e onde podem ser aplicados.