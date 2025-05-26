# Todos os programas na HP 12c Platinum

A tabela a seguir apresenta todos os programas deste repositório instalados na memória RAM da calculadora HP 12c Platinum, que suporta até 399 linhas de código (em comparação com o limite de 99 linhas da versão padrão da HP 12c).

As linhas de 1 a 16 são reservadas para atalhos de acesso rápido a cada programa. Para acessar, por exemplo, o Programa 3, basta digitar `GTO 003` e pressionar `R/S`. Esse recurso elimina a necessidade de memorizar a linha inicial de cada programa, tornando o uso de múltiplos programas mais prático e eficiente.

Além disso, cada programa é configurado para retornar automaticamente à sua linha inicial após a execução. Assim, ao pressionar R/S após o término do Programa 3, por exemplo, ele será executado novamente. Esse recurso facilita a reexecução do programa selecionado.

A tabela abaixo inclui os programas:
- Programa 001 (início na linha 17): [Calculadora de Juros Equivalentes](./01-juros-equivalentes.md)
- Programa 002 (início na linha 33): [Amortização pelo Sistema Francês (Tabela Price)](./01-juros-equivalentes.md)
- Programa 003 (início na linha 88): [Amortização pelo Sistema de Amortização Constante (Tabela SAC)](./03-tabela-sac.md)

| Linha | Instrução | Mostrador |
| :---: | :-------: | --------- |
|  01   |  GTO 017  | 43.33.017 |
|  02   |  GTO 033  | 43.33.033 |
|  03   |  GTO 088  | 43.33.088 |
|  04   |  GTO 000  | 43.33.000 |
|  05   |  GTO 000  | 43.33.000 |
|  06   |  GTO 000  | 43.33.000 |
|  07   |  GTO 000  | 43.33.000 |
|  08   |  GTO 000  | 43.33.000 |
|  09   |  GTO 000  | 43.33.000 |
|  10   |  GTO 000  | 43.33.000 |
|  11   |  GTO 000  | 43.33.000 |
|  12   |  GTO 000  | 43.33.000 |
|  13   |  GTO 000  | 43.33.000 |
|  14   |  GTO 000  | 43.33.000 |
|  15   |  GTO 000  | 43.33.000 |
|  16   |  GTO 000  | 43.33.000 |
|  17   |     1     | 01        |
|  18   |   RCL i   | 45.12     |
|  19   |     %     | 25        |
|  20   |     +     | 40        |
|  21   |   x><y    | 34        |
|  22   |   RCL n   | 45.11     |
|  23   |     /     | 10        |
|  24   |    y^x    | 21        |
|  25   |     1     | 01        |
|  26   |     -     | 30        |
|  27   |    EEX    | 26        |
|  28   |     2     | 02        |
|  29   |     x     | 20        |
|  30   |   STO i   | 44.12     |
|  31   |    R/S    | 31        |
|  32   |  GTO 001  | 43.33.001 |
|  33   |   STO 3   | 44.03     |
|  34   |     1     | 01        |
|  35   |   RCL i   | 45.12     |
|  36   |     %     | 25        |
|  37   |     +     | 40        |
|  38   |   RCL n   | 45.11     |
|  39   |    y^x    | 21        |
|  40   |   STO 4   | 44.04     |
|  41   |  RCL PV   | 45.13     |
|  42   |   STO 0   | 44.00     |
|  43   |   RCL i   | 45.12     |
|  44   |     %     | 25        |
|  45   |   RCL 4   | 45.04     |
|  46   |     x     | 20        |
|  47   |   RCL 4   | 45.04     |
|  48   |     1     | 01        |
|  49   |     -     | 30        |
|  50   |     /     | 10        |
|  51   |    CHS    | 16        |
|  52   |  STO PMT  | 44.14     |
|  53   |     1     | 01        |
|  54   |   RCL i   | 45.12     |
|  55   |     %     | 25        |
|  56   |     +     | 40        |
|  57   |   RCL 3   | 45.03     |
|  58   |    y^x    | 21        |
|  59   |   RCL 4   | 45.04     |
|  60   |   x><y    | 34        |
|  61   |     -     | 30        |
|  62   |   RCL 4   | 45.04     |
|  63   |     1     | 01        |
|  64   |     -     | 30        |
|  65   |     /     | 10        |
|  66   |   RCL 0   | 45.00     |
|  67   |     x     | 20        |
|  68   |  STO PV   | 44.13     |
|  69   |   RCL n   | 45.11     |
|  70   |   RCL 3   | 45.03     |
|  71   |     -     | 30        |
|  72   |   STO n   | 44.11     |
|  73   |   RCL 0   | 45.00     |
|  74   |    CHS    | 16        |
|  75   |  RCL PV   | 45.13     |
|  76   |     +     | 40        |
|  77   |   STO 2   | 44.02     |
|  78   |  RCL PMT  | 45.14     |
|  79   |   RCL 3   | 45.03     |
|  80   |     x     | 20        |
|  81   |   RCL 0   | 45.00     |
|  82   |  RCL PV   | 45.13     |
|  83   |     -     | 30        |
|  84   |     +     | 40        |
|  85   |   STO 1   | 44.01     |
|  86   |    R/S    | 31        |
|  87   |  GTO 002  | 43.33.002 |
|  88   |   STO 3   | 44.03     |
|  89   |  RCL PV   | 45.13     |
|  90   |   RCL i   | 45.12     |
|  91   |     %     | 25        |
|  92   |    CHS    | 16        |
|  93   |   STO 1   | 44.01     |
|  94   |  RCL PV   | 45.13     |
|  95   |   RCL n   | 45.11     |
|  96   |     /     | 10        |
|  97   |    CHS    | 16        |
|  98   |   STO 0   | 44.00     |
|  99   |   RCL i   | 45.12     |
|  100  |     %     | 25        |
|  101  |   RCL 3   | 45.03     |
|  102  |     1     | 01        |
|  103  |     -     | 30        |
|  104  |     x     | 20        |
|  105  |   RCL 1   | 45.01     |
|  106  |   x><y    | 34        |
|  107  |     -     | 30        |
|  108  |   STO 4   | 44.04     |
|  109  |   RCL 0   | 45.00     |
|  110  |     +     | 40        |
|  111  |  STO PMT  | 44.14     |
|  112  |   RCL n   | 45.11     |
|  113  |   RCL 3   | 45.03     |
|  114  |     -     | 30        |
|  115  |   STO n   | 44.11     |
|  116  |   RCL 0   | 45.00     |
|  117  |   RCL 3   | 45.03     |
|  118  |     x     | 20        |
|  119  |   STO 2   | 44.02     |
|  120  |  RCL PV   | 45.13     |
|  121  |     +     | 40        |
|  122  |  STO PV   | 44.13     |
|  123  |   RCL 2   | 45.02     |
|  124  |   RCL 1   | 45.01     |
|  125  |   RCL 4   | 45.04     |
|  126  |     +     | 40        |
|  127  |   RCL 3   | 45.03     |
|  128  |     x     | 20        |
|  129  |     2     | 02        |
|  130  |     /     | 10        |
|  131  |   STO 1   | 44.01     |
|  132  |    R/S    | 31        |
|  133  |  GTO 003  | 43.33.003 |
