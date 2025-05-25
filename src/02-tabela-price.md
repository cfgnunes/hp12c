# Amortização pelo Sistema Francês (Tabela Price)

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

| Ordem | Teclas  | Mostrador |
| :---: | :-----: | --------- |
|   1   |  STO 3  | 44.03     |
|   2   |    1    | 01        |
|   3   |  RCL i  | 45.12     |
|   4   |    %    | 25        |
|   5   |    +    | 40        |
|   6   |  RCL n  | 45.11     |
|   7   |   y^x   | 21        |
|   8   |  STO 4  | 44.04     |
|   9   | RCL PV  | 45.13     |
|  10   |  STO 0  | 44.00     |
|  11   |  RCL i  | 45.12     |
|  12   |    %    | 25        |
|  13   |  RCL 4  | 45.04     |
|  14   |    x    | 20        |
|  15   |  RCL 4  | 45.04     |
|  16   |    1    | 01        |
|  17   |    -    | 30        |
|  18   |    /    | 10        |
|  19   |   CHS   | 16        |
|  20   | STO PMT | 44.14     |
|  21   |    1    | 01        |
|  22   |  RCL i  | 45.12     |
|  23   |    %    | 25        |
|  24   |    +    | 40        |
|  25   |  RCL 3  | 45.03     |
|  26   |   y^x   | 21        |
|  27   |  RCL 4  | 45.04     |
|  28   |  x><y   | 34        |
|  29   |    -    | 30        |
|  30   |  RCL 4  | 45.04     |
|  31   |    1    | 01        |
|  32   |    -    | 30        |
|  33   |    /    | 10        |
|  34   |  RCL 0  | 45.00     |
|  35   |    x    | 20        |
|  36   | STO PV  | 44.13     |
|  37   |  RCL n  | 45.11     |
|  38   |  RCL 3  | 45.03     |
|  39   |    -    | 30        |
|  40   |  STO n  | 44.11     |
|  41   |  RCL 0  | 45.00     |
|  42   |   CHS   | 16        |
|  43   | RCL PV  | 45.13     |
|  44   |    +    | 40        |
|  45   |  STO 2  | 44.02     |
|  46   | RCL PMT | 45.14     |
|  47   |  RCL 3  | 45.03     |
|  48   |    x    | 20        |
|  49   |  RCL 0  | 45.00     |
|  50   | RCL PV  | 45.13     |
|  51   |    -    | 30        |
|  52   |    +    | 40        |
|  53   |  STO 1  | 44.01     |

## Exemplos de utilização do programa
