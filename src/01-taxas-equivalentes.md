# Taxas Equivalentes

Este programa realiza o cálculo de taxas de juros equivalentes entre diferentes períodos de capitalização. A funcionalidade é especialmente útil quando se deseja converter uma taxa mensal para anual, anual para mensal, ou entre quaisquer outras periodicidades.

## Entradas e saídas do programa

**Entradas:**
- i = taxa de juros atual.
- n = período da taxa atual.
- X = novo período desejado.

**Saídas:**
- i e X = taxa de juros equivalente para o novo período.

## Código do programa

| Ordem | Instrução | Mostrador |
| :---: | :-------: | --------- |
|   1   |     1     | 01        |
|   2   |   RCL i   | 45.12     |
|   3   |     %     | 25        |
|   4   |     +     | 40        |
|   5   |   x><y    | 34        |
|   6   |   RCL n   | 45.11     |
|   7   |     /     | 10        |
|   8   |    y^x    | 21        |
|   9   |     1     | 01        |
|  10   |     -     | 30        |
|  11   |    EEX    | 26        |
|  12   |     2     | 02        |
|  13   |     x     | 20        |
|  14   |   STO i   | 44.12     |

## Fórmula utilizada no programa

$$
i_X = \left(1 + i_n \right)^{\frac{n}{X}} - 1
$$

Onde:

- $i_n$ = taxa de juros atual (em decimal).
- $n$ = período da taxa atual (ex: 12 para taxa anual).
- $X$ = novo período desejado (ex: 1 para taxa mensal).
- $i_X$ =  taxa de juros equivalente para o novo período.

## Exemplos de utilização do programa

### Exemplo 1

**Você possui uma taxa de 1% ao mês e deseja saber qual é a taxa anual equivalente.**

Pressione as teclas:

```
1  [i]
1  [n]
12 [R/S]
```

O visor exibirá: 12,68 (taxa equivalente anual).

### Exemplo 2

**Você possui uma taxa de 12% ao ano e deseja saber qual é a taxa mensal equivalente.**

Pressione as teclas:

```
12 [i]
12 [n]
1  [R/S]
```

O visor exibirá: 0,95 (taxa equivalente mensal).
