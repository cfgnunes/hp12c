# Conversão entre taxas equivalentes

Este programa realiza o cálculo de taxas de juros equivalentes entre diferentes períodos de capitalização. A funcionalidade é especialmente útil quando se deseja converter uma taxa mensal para anual, anual para mensal, ou entre quaisquer outras periodicidades.

## Entradas e saídas do programa

**Entradas:**
- i = taxa de juros atual.
- n = período da taxa atual.
- X = novo período desejado.

**Saídas:**
- i e X = taxa de juros equivalente para o novo período.

## Código do programa

| Linha | Instrução | Mostrador | Comentário                             |
| :---: | :-------: | --------- | -------------------------------------- |
|  01   |    x=0    | 43.35     |                                        |
|  02   |  GTO 00   | 43.33.00  | Termina o programa se X = 0.           |
|  03   |     1     | 01        |                                        |
|  04   |   RCL i   | 45.12     |                                        |
|  05   |     %     | 25        |                                        |
|  06   |     +     | 40        |                                        |
|  07   |   x><y    | 34        |                                        |
|  08   |   RCL n   | 45.11     |                                        |
|  09   |    x=0    | 43.35     |                                        |
|  10   |  GTO 00   | 43.33.00  | Evita divisão por zero.                |
|  11   |     /     | 10        |                                        |
|  12   |    y^x    | 21        |                                        |
|  13   |     1     | 01        |                                        |
|  14   |     -     | 30        |                                        |
|  15   |    EEX    | 26        | Insere o valor 100 na pilha.           |
|  16   |     2     | 02        |                                        |
|  17   |     x     | 20        | Multiplica a taxa por 100.             |
|  18   |   STO i   | 44.12     | Armazena a nova taxa no registrador i. |

## Fórmula utilizada no programa

$$
i_X = \left(1 + i_n \right)^{\frac{X}{n}} - 1
$$

Onde:

- $i_n$ = taxa de juros atual (em decimal).
- $n$ = período da taxa atual (ex: 12 para taxa anual).
- $X$ = novo período desejado (ex: 1 para taxa mensal).
- $i_X$ =  taxa de juros equivalente para o novo período.

## Exemplos de utilização do programa

**Problema: Você possui uma taxa de 1% ao mês e deseja saber qual é a taxa anual equivalente.**

Pressione as teclas:
```
1  [i]
1  [n]      (1 mês: período mensal)
12          (12 meses: período anual)
   [R/S]    (executa o programa)
```

O visor exibirá: 12,68 (taxa equivalente anual).

**Problema: Você possui uma taxa de 12% ao ano e deseja saber qual é a taxa mensal equivalente.**

Pressione as teclas:
```
12 [i]
12 [n]      (12 meses: período anual)
1           (1 mês: período mensal)
   [R/S]    (executa o programa)
```

O visor exibirá: 0,95 (taxa equivalente mensal).
