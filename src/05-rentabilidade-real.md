# Cálculo de rentabilidade real

Este programa calcula a taxa real de juros, isto é, a rentabilidade efetiva de um investimento após descontar os efeitos da inflação.

## Entradas e saídas do programa

**Entradas:**
- i = taxa nominal de juros.
- X = taxa de inflação.

**Saídas:**
- i e X = taxa real de juros.

## Código do programa

| Linha | Instrução | Mostrador | Comentário                             |
| :---: | :-------: | --------- | -------------------------------------- |
|  01   |     1     | 01        |                                        |
|  02   |   x><y    | 34        |                                        |
|  03   |     %     | 25        |                                        |
|  04   |     +     | 40        |                                        |
|  05   |     1     | 01        |                                        |
|  06   |   RCL i   | 45.12     |                                        |
|  07   |     %     | 25        |                                        |
|  08   |     +     | 40        |                                        |
|  09   |   x><y    | 34        |                                        |
|  10   |    x=0    | 43.35     |                                        |
|  11   |  GTO 00   | 43.33.00  | Evita divisão por zero.                |
|  12   |     /     | 10        |                                        |
|  13   |     1     | 01        |                                        |
|  14   |     -     | 30        |                                        |
|  15   |    EEX    | 26        | Insere o valor 100 na pilha.           |
|  16   |     2     | 02        |                                        |
|  17   |     x     | 20        | Multiplica a taxa por 100.             |
|  18   |   STO i   | 44.12     | Armazena a nova taxa no registrador i. |


## Fórmula utilizada no programa

$$
r = \frac{1 + i}{1 + f} - 1
$$

Onde:

- $r$ = taxa real de juros (em decimal).
- $i$ = taxa nominal de juros (em decimal).
- $f$ = taxa de inflação (em decimal).

## Exemplos de utilização do programa

**Problema: Um banco informou que a rentabilidade de um determinado investimento foi de 12% ao ano, correspondendo aos juros nominais. No mesmo período, a inflação acumulada foi de 5%. Calcule os juros reais, ou seja, a rentabilidade efetiva do investimento descontando-se a inflação.**

Pressione as teclas:
```
12 [i]
5
   [R/S]    (executa o programa)
```

Resposta: 6,67% (taxa real de juros).
