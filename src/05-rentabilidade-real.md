# Rentabilidade Real

Este programa calcula a taxa real de juros, isto é, a rentabilidade efetiva de um investimento após descontar os efeitos da inflação.

## Entradas e saídas do programa

**Entradas:**
- i = taxa nominal de juros.
- X = taxa de inflação.

**Saídas:**
- i e X = taxa real de juros.

## Código do programa

| Ordem | Instrução | Mostrador |
| :---: | :-------: | --------- |
|   1   |     1     | 01        |
|   2   |   x><y    | 34        |
|   3   |     %     | 25        |
|   4   |     +     | 40        |
|   5   |     1     | 01        |
|   6   |   RCL i   | 45.12     |
|   7   |     %     | 25        |
|   8   |     +     | 40        |
|   9   |   x><y    | 34        |
|  10   |     /     | 10        |
|  11   |     1     | 01        |
|  12   |     -     | 30        |
|  13   |    EEX    | 26        |
|  14   |     2     | 02        |
|  15   |     x     | 20        |
|  16   |   STO i   | 44.12     |

## Fórmulas utilizadas no programa

$$
r = \frac{1 + i}{1 + f} - 1
$$

Onde:

- $r$ = taxa real de juros (em decimal).
- $i$ = taxa nominal de juros (em decimal).
- $f$ = taxa de inflação (em decimal).

## Exemplos de utilização do programa

### Exemplo 1

**Um banco informou que a rentabilidade de um determinado investimento foi de 12% ao ano, correspondendo aos juros nominais. No mesmo período, a inflação acumulada foi de 5%. Calcule os juros reais, ou seja, a rentabilidade efetiva do investimento descontando-se a inflação.**

Pressione as teclas:

```
12 i
5 R/S
```

O visor exibirá: 6,67 (taxa real de juros).
