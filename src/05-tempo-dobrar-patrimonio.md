# Tempo para Dobrar Patrimônio

## Entradas e saídas do programa

**Entradas:**
- i = taxa de juros (por período).

**Saídas:**
- X = tempo calculado (em períodos)

## Código do programa

| Ordem | Instrução | Mostrador |
| :---: | :-------: | --------- |
|   1   |     2     | 02        |
|   2   |    LN     | 43.23     |
|   3   |     1     | 01        |
|   4   |   RCL i   | 45.12     |
|   5   |     %     | 25        |
|   6   |     +     | 40        |
|   7   |    LN     | 43.23     |
|   8   |     /     | 10        |

## Fórmulas utilizadas no programa

$$
X = \frac{\ln(2)}{\ln(1 + i)}
$$

Onde:

- $i$ = taxa de juros por período (ex: 8% anual).
- $X$ = tempo calculado (em períodos, ex: anos).

## Exemplos de utilização do programa

### Exemplo 1

**Em quanto tempo uma taxa de juros anual de 8% dobraria o seu patrimônio?**

Pressione as teclas:

```
8 i
R/S
```

Então o visor exibirá: `9,01` (aproximadamente 9 anos para dobrar o patrimônio).

### Exemplo 2

**Em quanto tempo uma taxa de juros mensal de 2,6% dobraria o seu patrimônio?**

Pressione as teclas:

```
2,6 i
R/S
```

Então o visor exibirá: `27,00` (27 meses para dobrar o patrimônio).
