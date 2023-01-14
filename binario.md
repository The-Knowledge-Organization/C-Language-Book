
## Bit

Um `Bit` é a forma mais básica possível para se representar dados. Um bit pode conter o apenas o valor 0 ou 1.
Usando uma cadeia de bits podemos representar números, usando a base binária(2).
Estamos habituados a conviver com a base decimal(10), que varia dos números 0-9, mas o computador não tem tudo isso, apenas zeros e uns, então, como os números são armazenados?

Imagine num país hipotético em que o sistema de moedas funciona da seguinte forma:

- A moeda de mais baixo valor é 1
- A próxima nota é o dobro do valor da anterior.

Por exempo, as cinco notas com valor mais baixo deste país são:
1 -> 2 -> 4 -> 8 -> 16.
.
## Tamanho

Imagine que você é um cidadão desse país hipotético, e que possui apenas uma as quatro primeiras notas (1, 2, 4 e 8). Quanto você tem no total? Para saber isso você poderia somar todos os valores, 1 + 2 + 4 + 8 = 15, não está errado, mas existe uma formula mais fácil para cálcular a quantidade máxima, basta usar `2^n - 1`, onde `n` é o número de notas que possui. Desta forma temos: 2^4 => 16 - 1 = 15. 

Usando somente essas 4 notas você é capaz de representar qualquer valor entre 0 e 15, basta usar a combinação correta de notas.

## Representando Números

Imagine que você queira comprar um sorvete, e que este custa `$B 3`. Para comprar basta usar a nota de `1` e `2`. , agora imagine que outro produto custe `$B 13`, a primeira vista pode parecer que não tem como comprar o produto sem precisar que o vendedor tenha troco, mas espere um momento. Se combinarmos as notas de `8`, `4` e `1`. teremos exatamente `$B 13`.

Mas onde isso se conecta a binário? Vamos traduzir as transações acima para binário. Basicamente vamos dizer que: 

- Cada nota é equivale a um bit, então 4 notas são 4 bits.
- Por padrão, todos os bits tem o valor de 0.
- Ao usarmos uma nota o valor do bit muda para 1, caso contrário o valor se mantem como 0.
- O valor mais baixo da moeda fica na direita, enquanto o maior na esquerda.

Para representar a compra do sorvete em binária faremos:

|    |      |	 	| |      |	 	| 
|  :--	  |    --    |	  --	| -- | --: | 
|  Moeda	  |	   8    |	  4	|	  2	| 1	|
|  Bits   |	   0    |	  0	| 1	| 1	|

Está aí, o valor de `3` em binário é `0011`, agora para reprentar a compra de `$B 13`:

|    |      |	 	| |      |	 	| 
|  :--	  |    --    |	  --	| -- | --: | 
|  Moeda	  |	   8    |	  4	|	  2	| 1	|
|  Bits   |	   1    |	  1	| 0	| 1	|

E é desta forma que representamos o número `13` em binário. Bem simple não?

## Byte

Um byte é simplesmente 8 bits em sequencia, então com 1 bytes podemos representar 2^8 números, ou 256 (contando com o 0).

Se adicionarmos 1 bit a mais no byte, irmos de 8 para 9, o valor máximo **dobra**, de 256 números passamos para 512. Isso parece trivial, porem as coisas ficam não intruítivas quando dobramos o número de bits, pois ao fazer isso o número máximo que podemos representar é elevado ao quadrado.
Ou seja, se pularmos de 1 byte (8 bits) para 2 bytes (16 bits). Vamos de 256 números para **65536**, um salto enorme.

## Uso

O tipo Int geralmente representa um inteiro de 32 bits (ou 4 bytes). Isso o torna capaz de representar `4294967296` números diferentes, um número realmente grande, porem não é nem o maior, o tipo `long` é capaz de representar 64 bits (ou 8 bytes), que são os absurdos `1.8446744073709552e+19`. Mas Denovo, ele ainda não é o maior. Algumas linguagens suportam o `long long`, ou seja, 128 bits (ou 16 bytes), `3.402823669209385e+38`,  um pouco mais de 3 quatrilhões.

## Números Negativos

Para representar os números negativos usamos o 0 mais a esquerda. Vamos usar como exeplo um simples número de 4 bits.

Como vimos antes, um número de 4 bits pode representar 16 números diferentes (incluindo o 0), porem, todos esses são positivos. Para os números negativos alocamos o bit mais a esquerda como sinal, se for 0 então o número é positivo, se for 1 o número é negativo.
Mas isso tem implicações, como o bit mais a esquerda não representa mais um número, o valor máximo que podemos representar é `2^3 - 1`  => 7. Veja:

|    |      |	 	| |      |	 	| 
|  :--	  |    --    |	  --	| -- | --: | 
|  Moeda	  |	   sinal    |	  4	|	  2	| 1	|
|  Bits   |	   0    |	  1	| 1	| 1	|

O valor máximo se torna 7. Porem, se mudarmos o bit de `sinal` para `1` podemos represenar números negativos até `-7`, então fazemos uma troca, metade do valor máximo para poder usar números abaixo de 0.

É por isso que algumas linguagens tem suporte para `signed` e `unsigned`, ao usar unsigned, estamos dizendo para a linguagem que não queremos esse bit de sinal, e que um valor deve ser usado no lugar dele. `Signed` é o valor padrão e usa esse bit de sinal.