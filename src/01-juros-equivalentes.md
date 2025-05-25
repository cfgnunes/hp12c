# Taxas de Juros Equivalentes

## Entradas e saídas do programa

**Entradas:**
- i = taxa de juros atual.
- n = período da taxa atual.
- X = novo período desejado.

**Saídas:**
- i e X = taxa de juros equivalente para o novo período.

## Código do programa

| Ordem | Teclas | Mostrador | Comentário                                                            |
| :---: | :----: | --------- | --------------------------------------------------------------------- |
|   1   |   1    | 01        |                                                                       |
|   2   | RCL i  | 45.12     | Recupera o valor da taxa de juros atual armazenado no registrador i.  |
|   3   |   %    | 25        | Converte a taxa de juros de percentual para decimal (divide por 100). |
|   4   |   +    | 40        | Soma 1 ao valor convertido (1 + i).                                   |
|   5   |  x><y  | 34        | Troca os elementos X e Y da pilha, preparando para divisão.           |
|   6   | RCL n  | 45.11     | Recupera o período da taxa atual (n).                                 |
|   7   |   /    | 10        | Divide n por X.                                                       |
|   8   |  y^x   | 21        | Eleva (1 + i) à potência (n / X).                                     |
|   9   |   1    | 01        | Insere 1 na pilha.                                                    |
|  10   |   -    | 30        | Subtrai 1 do resultado  [(1 + i)^(n/X)] - 1.                          |
|  11   |  EEX   | 26        |                                                                       |
|  12   |   2    | 02        |                                                                       |
|  13   |   x    | 20        | Multiplica por 100: converte o resultado de volta para porcentagem.   |
|  14   | STO i  | 44.12     | Armazena a nova taxa de juros no registrador i.                       |

## Fórmulas utilizadas no programa

A fórmula para calcular taxas de juros equivalentes entre dois períodos de capitalização diferentes é:

$$
i_X = \left( \left(1 + \frac{i_n}{100} \right)^{\frac{n}{X}} - 1 \right) \times 100
$$

Onde:

* $i_n$ = taxa de juros atual (ex: 5%).
* $n$ = período da taxa atual (ex: 12 para taxa anual).
* $X$ = novo período desejado (ex: 1 para taxa mensal).
* $i_X$ =  taxa de juros equivalente para o novo período.

## Exemplos de utilização do programa

### Exemplo 1

**Você possui uma taxa de 1% ao mês e deseja saber qual é a taxa anual equivalente.**

Pressione as teclas:

```
1 i
1 n
12 R/S
```

Então o visor exibirá: `12,68` (taxa equivalente anual).

### Exemplo 2

**Você possui uma taxa de 12% ao ano e deseja saber qual é a taxa mensal equivalente.**

Pressione as teclas:

```
12 i
12 n
1 R/S
```

Então o visor exibirá: `0,95 %` (taxa equivalente mensal).
