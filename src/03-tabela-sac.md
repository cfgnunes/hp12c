# Amortização pelo Sistema de Amortização Constante (Tabela SAC)

## Entradas e saídas do programa

**Entradas:**
- n = quantidade total de períodos.
- i = taxa de juros.
- PV = valor do empréstimo (principal).
- X = quantidade de pagamentos (períodos) a serem amortizados.

**Saídas:**
- n = quantidade de períodos restantes.
- PV = saldo devedor restante.
- PMT = valor da parcela.
- Y e R2 = total do principal até o período amortizado.
- X e R1 = total de juros até o período amortizado.
- R0 = valor da amortização constante.

**Nota:** Pressione + para exibir o valor total pago (principal + juros).

## Código do programa

| Ordem | Teclas  | Mostrador |
| :---: | :-----: | --------- |
|   1   |  STO 3  | 44.03     |
|   2   | RCL PV  | 45.13     |
|   3   |  RCL i  | 45.12     |
|   4   |    %    | 25        |
|   5   |   CHS   | 16        |
|   6   |  STO 1  | 44.01     |
|   7   | RCL PV  | 45.13     |
|   8   |  RCL n  | 45.11     |
|   9   |    /    | 10        |
|  10   |   CHS   | 16        |
|  11   |  STO 0  | 44.00     |
|  12   |  RCL i  | 45.12     |
|  13   |    %    | 25        |
|  14   |  RCL 3  | 45.03     |
|  15   |    1    | 01        |
|  16   |    -    | 30        |
|  17   |    x    | 20        |
|  18   |  RCL 1  | 45.01     |
|  19   |  x><y   | 34        |
|  20   |    -    | 30        |
|  21   |  STO 4  | 44.04     |
|  22   |  RCL 0  | 45.00     |
|  23   |    +    | 40        |
|  24   | STO PMT | 44.14     |
|  25   |  RCL n  | 45.11     |
|  26   |  RCL 3  | 45.03     |
|  27   |    -    | 30        |
|  28   |  STO n  | 44.11     |
|  29   |  RCL 0  | 45.00     |
|  30   |  RCL 3  | 45.03     |
|  31   |    x    | 20        |
|  32   |  STO 2  | 44.02     |
|  33   | RCL PV  | 45.13     |
|  34   |    +    | 40        |
|  35   | STO PV  | 44.13     |
|  36   |  RCL 2  | 45.02     |
|  37   |  RCL 1  | 45.01     |
|  38   |  RCL 4  | 45.04     |
|  39   |    +    | 40        |
|  40   |  RCL 3  | 45.03     |
|  41   |    x    | 20        |
|  42   |    2    | 02        |
|  43   |    /    | 10        |
|  44   |  STO 1  | 44.01     |

## Exemplos de utilização do programa

### Exemplo 1

**Em um empréstimo de R$500.000,00, com taxa de 2% ao mês, pelo prazo de 20 meses, pede-se:**

**a) Calcule o total de juros pagos até a 13ª parcela.**

Pressione as teclas:

```
20 n
2 i
500000 PV
13 R/S
```

O visor exibirá: `-91.000,00` (total de juros pagos até a 13ª parcela).

**b) Calcule o total pago até a 13ª parcela.**

Pressione a tecla `+`

O visor exibirá: `-416.000,00` (total pago até a 13ª parcela).

### Exemplo 2

**Em um empréstimo de R$350.000,00, com taxa de 1% ao mês, por 35 meses, pede-se:**

**a) Calcule os juros pagos somente na 28ª parcela.**

Acumule as amortizações até a 27ª parcela, pressionando as teclas:

```
350000 PV
1 i
35 n
27 R/S
```

Em seguida, calcule somente a parcela 28, pressionando as teclas:

```
1 R/S
```

O visor exibirá: `-800,00` (juros pagos somente na 28ª parcela).


**b) Calcule o valor da 28ª parcela.**

Pressione as teclas:

```
RCL PMT
```

O visor exibirá: `-10.800,00` (valor da 28ª parcela).

### Exemplo 3

**Em um empréstimo de R$320.000,00, com taxa de 3% ao mês, por 42 meses, pede-se:**

**a) Calcule o total de juros pagos ao longo de todo o financiamento.**

Pressione as teclas:

```
320000 PV
3 i
42 n
42 R/S
```

O visor exibirá: `-206.400,00` (total de juros pagos durante todo o financiamento).


**b) Calcule o total das parcelas ao longo de todo o financiamento.**

Pressione a tecla `+`

O visor exibirá: `-526.400,00` (total pago em parcelas ao longo de todo o financiamento).

### Exemplo 4

**Em um empréstimo de R$260.000,00, com taxa de 4% ao mês, por 38 meses, pede-se:**

**a) Calcule o total de juros pagos entre a 16ª e a 27ª parcela.**

Primeiro, amortize até a 15ª parcela, pressionando as teclas:

```
260000 PV
4 i
38 n
15 R/S
```

Em seguida, amortize da 16ª até a 27ª parcela (12 parcelas), pressionando as teclas:

```
12 R/S
```

O visor exibirá: `-57.473,68` (total de juros pagos entre a 16ª e 27ª parcela).

**b) Calcule o total de amortizações entre a 16ª e a 27ª parcela.**

Pressione a tecla `x><y`

O visor exibirá: `-82.105,26` (total de capital amortizado nesse período).

**c) Calcule o total pago entre a 16ª e a 27ª parcela.**

Pressione a tecla `+`

O visor exibirá: `-139.578,95` (total pago em parcelas da 16ª à 27ª).
