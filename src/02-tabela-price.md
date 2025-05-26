# Amortização pelo Sistema Francês (Tabela Price)

Este programa calcula, com exatidão, os principais valores envolvidos na amortização de empréstimos pelo Sistema Francês, também conhecido como Tabela Price. Ele permite calcular o saldo devedor, o total de juros pagos, o valor amortizado e o valor total desembolsado em qualquer ponto do financiamento.

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

**Nota:** Pressione + para exibir o valor total pago (principal + juros).

## Código do programa

| Ordem | Instrução | Mostrador |
| :---: | :-------: | --------- |
|   1   |   STO 3   | 44.03     |
|   2   |     1     | 01        |
|   3   |   RCL i   | 45.12     |
|   4   |     %     | 25        |
|   5   |     +     | 40        |
|   6   |   RCL n   | 45.11     |
|   7   |    y^x    | 21        |
|   8   |   STO 4   | 44.04     |
|   9   |  RCL PV   | 45.13     |
|  10   |   STO 0   | 44.00     |
|  11   |   RCL i   | 45.12     |
|  12   |     %     | 25        |
|  13   |   RCL 4   | 45.04     |
|  14   |     x     | 20        |
|  15   |   RCL 4   | 45.04     |
|  16   |     1     | 01        |
|  17   |     -     | 30        |
|  18   |     /     | 10        |
|  19   |    CHS    | 16        |
|  20   |  STO PMT  | 44.14     |
|  21   |     1     | 01        |
|  22   |   RCL i   | 45.12     |
|  23   |     %     | 25        |
|  24   |     +     | 40        |
|  25   |   RCL 3   | 45.03     |
|  26   |    y^x    | 21        |
|  27   |   RCL 4   | 45.04     |
|  28   |   x><y    | 34        |
|  29   |     -     | 30        |
|  30   |   RCL 4   | 45.04     |
|  31   |     1     | 01        |
|  32   |     -     | 30        |
|  33   |     /     | 10        |
|  34   |   RCL 0   | 45.00     |
|  35   |     x     | 20        |
|  36   |  STO PV   | 44.13     |
|  37   |   RCL n   | 45.11     |
|  38   |   RCL 3   | 45.03     |
|  39   |     -     | 30        |
|  40   |   STO n   | 44.11     |
|  41   |   RCL 0   | 45.00     |
|  42   |    CHS    | 16        |
|  43   |  RCL PV   | 45.13     |
|  44   |     +     | 40        |
|  45   |   STO 2   | 44.02     |
|  46   |  RCL PMT  | 45.14     |
|  47   |   RCL 3   | 45.03     |
|  48   |     x     | 20        |
|  49   |   RCL 0   | 45.00     |
|  50   |  RCL PV   | 45.13     |
|  51   |     -     | 30        |
|  52   |     +     | 40        |
|  53   |   STO 1   | 44.01     |

## Fórmulas utilizadas no programa

1. Parcela (PMT):

$$
PMT = PV \cdot \frac{i(1+i)^n}{(1+i)^n - 1}
$$

2. Saldo devedor no período $t$:

$$
SD_t = PV \cdot \frac{(1+i)^n - (1+i)^t}{(1+i)^n - 1}
$$

3. Valor principal acumulados até o período $t$:

$$
Amort_t = PV - SD_t
$$

4. Valor de juros acumulados até o período $t$:

$$
J_t = PMT \cdot t - \left(PV - SD_t\right)
$$

Onde:

- $i$ = taxa de juros.
- $n$ = quantidade total de períodos.
- $t$ = quantidade de pagamentos (períodos) a serem amortizados.
- $PV$ = valor do empréstimo (principal).
- $PMT$ = valor da parcela.

## Exemplos de utilização do programa

### Exemplo 1

**Considere um empréstimo de R$ 500.000,00, com taxa de juros de 2% ao mês e prazo total de 20 meses. Com base nessas condições, calcule o total de juros pagos até a 13ª parcela, bem como o valor total pago até essa mesma parcela.**

Pressione as teclas:

```
20 n
2 i
500000 PV
13 R/S
```

O visor exibirá: -95.421,53 (total de juros pagos até a 13ª parcela).

Pressione a tecla `+`

O visor exibirá: -397.518,67 (total pago até a 13ª parcela).

### Exemplo 2

**Considere um empréstimo no valor de R$350.000,00, com taxa de juros de 1% ao mês e prazo de 35 meses. Com base nesses dados, determine os juros pagos especificamente na 28ª parcela, bem como o valor total dessa parcela.**

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

O visor exibirá: -910,65 (juros pagos somente na 28ª parcela).

Pressione as teclas:

```
RCL PMT
```

O visor exibirá: -11.901,29 (valor da 28ª parcela).

### Exemplo 3

**Considere um empréstimo no valor de R$ 320.000,00, com taxa de juros de 3% ao mês e prazo total de 42 meses. Com base nessas condições, calcule o total de juros pagos ao longo de todo o financiamento, assim como o valor total desembolsado com o pagamento das parcelas durante todo o período.**

Pressione as teclas:

```
320000 PV
3 i
42 n
42 R/S
```

O visor exibirá: -247.056,09 (total de juros pagos durante todo o financiamento).

Pressione a tecla `+`

O visor exibirá: -567.056,09 (total pago em parcelas ao longo de todo o financiamento).

### Exemplo 4

**Considere um empréstimo no valor de R$260.000,00, com taxa de juros de 4% ao mês e prazo total de 38 meses. Com base nessas condições, calcule, para o período entre a 16ª e a 27ª parcela: o total de juros pagos, o total de amortizações realizadas e o valor total desembolsado com o pagamento dessas parcelas.**

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

O visor exibirá: -79.252,16 (total de juros pagos entre a 16ª e 27ª parcela).

Pressione a tecla `x><y`

O visor exibirá: -81.839,43 (total de capital amortizado nesse período).

Pressione a tecla `+`

O visor exibirá: -161.091,59 (total pago em parcelas da 16ª à 27ª).
