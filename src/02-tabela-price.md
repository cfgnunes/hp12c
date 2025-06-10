# Sistema de Amortização Francês (SAF)

Este sistema de amortização também é conhecido como "Tabela Price" ou "Sistema de Prestação Constante".

Este programa calcula, com exatidão, os principais valores envolvidos na amortização de empréstimos pelo Sistema Francês, também conhecido como Tabela Price. Ele permite calcular o saldo devedor, o total de juros pagos, o valor amortizado e o valor total desembolsado em qualquer ponto do financiamento.

## Entradas e saídas do programa

**Entradas:**
- n = número total de parcelas.
- i = taxa de juros.
- PV = valor do empréstimo (principal).
- X = número de parcelas a amortizar.

**Saídas:**
- n = número de parcelas restantes.
- PV = saldo devedor restante.
- PMT = valor da parcela.
- Y e R2 = total do principal até o período amortizado.
- X e R1 = total de juros até o período amortizado.

**Nota:** Pressione + para exibir o valor total pago (principal + juros).

## Código do programa

| Linha | Instrução | Mostrador | Comentário                                                               |
| :---: | :-------: | --------- | ------------------------------------------------------------------------ |
|  01   |   STO 3   | 44.03     | Armazena o número de parcelas a amortizar em R3.                         |
|  02   |     1     | 01        |                                                                          |
|  03   |   RCL i   | 45.12     |                                                                          |
|  04   |     %     | 25        |                                                                          |
|  05   |     +     | 40        |                                                                          |
|  06   |   RCL n   | 45.11     |                                                                          |
|  07   |    y^x    | 21        |                                                                          |
|  08   |   STO 4   | 44.04     | R4 = (i%+1)^n                                                            |
|  09   |  RCL PV   | 45.13     |                                                                          |
|  10   |   STO 0   | 44.00     | Armazena o valor do empréstimo (principal) em R0.                        |
|  11   |   RCL i   | 45.12     |                                                                          |
|  12   |     %     | 25        |                                                                          |
|  13   |   RCL 4   | 45.04     |                                                                          |
|  14   |     x     | 20        |                                                                          |
|  15   |   RCL 4   | 45.04     |                                                                          |
|  16   |     1     | 01        |                                                                          |
|  17   |     -     | 30        |                                                                          |
|  18   |    x=0    | 43.35     |                                                                          |
|  19   |  GTO 00   | 43.33.00  | Evita divisão por zero.                                                  |
|  20   |     /     | 10        |                                                                          |
|  21   |    CHS    | 16        |                                                                          |
|  22   |  STO PMT  | 44.14     | Armazena o valor da parcela: PMT = - (i% * R0 * R4) / (R4 - 1)           |
|  23   |     1     | 01        |                                                                          |
|  24   |   RCL i   | 45.12     |                                                                          |
|  25   |     %     | 25        |                                                                          |
|  26   |     +     | 40        |                                                                          |
|  27   |   RCL 3   | 45.03     |                                                                          |
|  28   |    y^x    | 21        |                                                                          |
|  29   |   RCL 4   | 45.04     |                                                                          |
|  30   |   x><y    | 34        |                                                                          |
|  31   |     -     | 30        |                                                                          |
|  32   |   RCL 4   | 45.04     |                                                                          |
|  33   |     1     | 01        |                                                                          |
|  34   |     -     | 30        |                                                                          |
|  35   |    x=0    | 43.35     |                                                                          |
|  36   |  GTO 00   | 43.33.00  | Evita divisão por zero.                                                  |
|  37   |     /     | 10        |                                                                          |
|  38   |   RCL 0   | 45.00     |                                                                          |
|  39   |     x     | 20        |                                                                          |
|  40   |  STO PV   | 44.13     | Armazena o saldo devedor restante: PV = (R4 - (i%+1)^R3) / (R4 - 1) * R0 |
|  41   |   RCL n   | 45.11     |                                                                          |
|  42   |   RCL 3   | 45.03     |                                                                          |
|  43   |     -     | 30        |                                                                          |
|  44   |   STO n   | 44.11     | Armazena o número de períodos restantes: n = n - R3                      |
|  45   |   RCL 0   | 45.00     |                                                                          |
|  46   |    CHS    | 16        |                                                                          |
|  47   |  RCL PV   | 45.13     |                                                                          |
|  48   |     +     | 40        | Empilha no registrador Y o valor do principal: -R0 + PV                  |
|  49   |   STO 2   | 44.02     | Também armazena em R2.                                                   |
|  50   |  RCL PMT  | 45.14     |                                                                          |
|  51   |   RCL 3   | 45.03     |                                                                          |
|  52   |     x     | 20        |                                                                          |
|  53   |   RCL 0   | 45.00     |                                                                          |
|  54   |  RCL PV   | 45.13     |                                                                          |
|  55   |     -     | 30        |                                                                          |
|  56   |     +     | 40        | Empilha no registrador X o valor dos juros: -PMT * R3 + (R0 - PV)        |
|  57   |   STO 1   | 44.01     | Também armazena em R1.                                                   |

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

**Problema: Considere um empréstimo de R$ 500.000,00, com taxa de juros de 2% ao mês e prazo total de 20 meses. Com base nessas condições, calcule o total de juros pagos até a 13ª parcela, bem como o valor total pago até essa mesma parcela.**

Pressione as teclas:
```
500000 [PV]
2      [i]
20     [n]
13     [R/S]
```

O visor exibirá: -95.421,53 (total de juros pagos até a 13ª parcela).

Pressione a tecla: `[+]`

O visor exibirá: -397.518,67 (total pago até a 13ª parcela).

**Problema: Considere um empréstimo no valor de R$350.000,00, com taxa de juros de 1% ao mês e prazo de 35 meses. Com base nesses dados, determine os juros pagos especificamente na 28ª parcela, bem como o valor total dessa parcela.**

Acumule as amortizações até a 27ª parcela, pressionando as teclas:
```
350000 [PV]
1      [i]
35     [n]
27
       [R/S]    (executa o programa)
```

Em seguida, calcule somente a parcela 28, pressionando as teclas:
```
1 [R/S]
```

O visor exibirá: -910,65 (juros pagos somente na 28ª parcela).

Pressione as teclas:
```
[RCL] [PMT]
```

O visor exibirá: -11.901,29 (valor da 28ª parcela).

**Problema: Considere um empréstimo no valor de R$ 320.000,00, com taxa de juros de 3% ao mês e prazo total de 42 meses. Com base nessas condições, calcule o total de juros pagos ao longo de todo o financiamento, assim como o valor total desembolsado com o pagamento das parcelas durante todo o período.**

Pressione as teclas:
```
320000 [PV]
3      [i]
42     [n]
42
       [R/S]    (executa o programa)
```

O visor exibirá: -247.056,09 (total de juros pagos durante todo o financiamento).

Pressione a tecla: `[+]`

O visor exibirá: -567.056,09 (total pago em parcelas ao longo de todo o financiamento).

**Problema: Considere um empréstimo no valor de R$260.000,00, com taxa de juros de 4% ao mês e prazo total de 38 meses. Com base nessas condições, calcule, para o período entre a 16ª e a 27ª parcela: o total de juros pagos, o total de amortizações realizadas e o valor total desembolsado com o pagamento dessas parcelas.**

Primeiro, amortize até a 15ª parcela, pressionando as teclas:
```
260000 [PV]
4      [i]
38     [n]
15
       [R/S]    (executa o programa)
```

Em seguida, amortize da 16ª até a 27ª parcela (12 parcelas), pressionando as teclas:
```
12 [R/S]
```

O visor exibirá: -79.252,16 (total de juros pagos entre a 16ª e 27ª parcela).

Pressione a tecla: `[x><y]`

O visor exibirá: -81.839,43 (total de capital amortizado nesse período).

Pressione a tecla: `[+]`

O visor exibirá: -161.091,59 (total pago em parcelas da 16ª à 27ª).
