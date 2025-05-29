# Todos os programas instalados na HP 12c Platinum

A tabela a seguir apresenta todos os programas deste repositório instalados na memória RAM da calculadora HP 12c Platinum, que suporta até 399 linhas de código (em comparação com o limite de 99 linhas da versão padrão da HP 12c).

As linhas de 1 a 16 são reservadas para atalhos de acesso rápido a cada programa. Para acessar, por exemplo, o Programa 3, basta digitar `GTO 003` e pressionar `R/S`. Esse recurso elimina a necessidade de memorizar a linha inicial de cada programa, tornando o uso de múltiplos programas mais prático e eficiente.

Além disso, cada programa é configurado para retornar automaticamente à sua linha inicial após a execução. Assim, ao pressionar R/S após o término do Programa 3, por exemplo, ele será executado novamente. Esse recurso facilita a reexecução do programa selecionado.

A tabela abaixo inclui os programas:
- Programa 001 (início na linha 017): [Taxas Equivalentes](./01-taxas-equivalentes.md)
- Programa 002 (início na linha 033): [Sistema de Amortização Francês (SAF)](./01-taxas-equivalentes.md)
- Programa 003 (início na linha 088): [Sistema de Amortização Constante (SAC)](./03-tabela-sac.md)
- Programa 004 (início na linha 134): [Prazo Fracionário](./04-prazo-fracionario.md)
- Programa 005 (início na linha 158): [Rentabilidade Real](./05-rentabilidade-real.md)

| Linha | Instrução | Mostrador | Comentário |
| :---: | :-------: | --------- | ---------- |
|  001  |  GTO 017  | 43.33.017 |            |
|  002  |  GTO 033  | 43.33.033 |            |
|  003  |  GTO 088  | 43.33.088 |            |
|  004  |  GTO 134  | 43.33.134 |            |
|  005  |  GTO 158  | 43.33.158 |            |
|  006  |  GTO 000  | 43.33.000 |            |
|  007  |  GTO 000  | 43.33.000 |            |
|  008  |  GTO 000  | 43.33.000 |            |
|  009  |  GTO 000  | 43.33.000 |            |
|  010  |  GTO 000  | 43.33.000 |            |
|  011  |  GTO 000  | 43.33.000 |            |
|  012  |  GTO 000  | 43.33.000 |            |
|  013  |  GTO 000  | 43.33.000 |            |
|  014  |  GTO 000  | 43.33.000 |            |
|  015  |  GTO 000  | 43.33.000 |            |
|  016  |  GTO 000  | 43.33.000 |            |
|  017  |     1     | 01        | Prog. 001  |
|  018  |   RCL i   | 45.12     |            |
|  019  |     %     | 25        |            |
|  020  |     +     | 40        |            |
|  021  |   x><y    | 34        |            |
|  022  |   RCL n   | 45.11     |            |
|  023  |     /     | 10        |            |
|  024  |    y^x    | 21        |            |
|  025  |     1     | 01        |            |
|  026  |     -     | 30        |            |
|  027  |    EEX    | 26        |            |
|  028  |     2     | 02        |            |
|  029  |     x     | 20        |            |
|  030  |   STO i   | 44.12     |            |
|  031  |    R/S    | 31        |            |
|  032  |  GTO 001  | 43.33.001 |            |
|  033  |   STO 3   | 44.03     | Prog. 002  |
|  034  |     1     | 01        |            |
|  035  |   RCL i   | 45.12     |            |
|  036  |     %     | 25        |            |
|  037  |     +     | 40        |            |
|  038  |   RCL n   | 45.11     |            |
|  039  |    y^x    | 21        |            |
|  040  |   STO 4   | 44.04     |            |
|  041  |  RCL PV   | 45.13     |            |
|  042  |   STO 0   | 44.00     |            |
|  043  |   RCL i   | 45.12     |            |
|  044  |     %     | 25        |            |
|  045  |   RCL 4   | 45.04     |            |
|  046  |     x     | 20        |            |
|  047  |   RCL 4   | 45.04     |            |
|  048  |     1     | 01        |            |
|  049  |     -     | 30        |            |
|  050  |     /     | 10        |            |
|  051  |    CHS    | 16        |            |
|  052  |  STO PMT  | 44.14     |            |
|  053  |     1     | 01        |            |
|  054  |   RCL i   | 45.12     |            |
|  055  |     %     | 25        |            |
|  056  |     +     | 40        |            |
|  057  |   RCL 3   | 45.03     |            |
|  058  |    y^x    | 21        |            |
|  059  |   RCL 4   | 45.04     |            |
|  060  |   x><y    | 34        |            |
|  061  |     -     | 30        |            |
|  062  |   RCL 4   | 45.04     |            |
|  063  |     1     | 01        |            |
|  064  |     -     | 30        |            |
|  065  |     /     | 10        |            |
|  066  |   RCL 0   | 45.00     |            |
|  067  |     x     | 20        |            |
|  068  |  STO PV   | 44.13     |            |
|  069  |   RCL n   | 45.11     |            |
|  070  |   RCL 3   | 45.03     |            |
|  071  |     -     | 30        |            |
|  072  |   STO n   | 44.11     |            |
|  073  |   RCL 0   | 45.00     |            |
|  074  |    CHS    | 16        |            |
|  075  |  RCL PV   | 45.13     |            |
|  076  |     +     | 40        |            |
|  077  |   STO 2   | 44.02     |            |
|  078  |  RCL PMT  | 45.14     |            |
|  079  |   RCL 3   | 45.03     |            |
|  080  |     x     | 20        |            |
|  081  |   RCL 0   | 45.00     |            |
|  082  |  RCL PV   | 45.13     |            |
|  083  |     -     | 30        |            |
|  084  |     +     | 40        |            |
|  085  |   STO 1   | 44.01     |            |
|  086  |    R/S    | 31        |            |
|  087  |  GTO 002  | 43.33.002 |            |
|  088  |   STO 3   | 44.03     | Prog. 003  |
|  089  |  RCL PV   | 45.13     |            |
|  090  |   RCL i   | 45.12     |            |
|  091  |     %     | 25        |            |
|  092  |    CHS    | 16        |            |
|  093  |   STO 1   | 44.01     |            |
|  094  |  RCL PV   | 45.13     |            |
|  095  |   RCL n   | 45.11     |            |
|  096  |     /     | 10        |            |
|  097  |    CHS    | 16        |            |
|  098  |   STO 0   | 44.00     |            |
|  099  |   RCL i   | 45.12     |            |
|  100  |     %     | 25        |            |
|  101  |   RCL 3   | 45.03     |            |
|  102  |     1     | 01        |            |
|  103  |     -     | 30        |            |
|  104  |     x     | 20        |            |
|  105  |   RCL 1   | 45.01     |            |
|  106  |   x><y    | 34        |            |
|  107  |     -     | 30        |            |
|  108  |   STO 4   | 44.04     |            |
|  109  |   RCL 0   | 45.00     |            |
|  110  |     +     | 40        |            |
|  111  |  STO PMT  | 44.14     |            |
|  112  |   RCL n   | 45.11     |            |
|  113  |   RCL 3   | 45.03     |            |
|  114  |     -     | 30        |            |
|  115  |   STO n   | 44.11     |            |
|  116  |   RCL 0   | 45.00     |            |
|  117  |   RCL 3   | 45.03     |            |
|  118  |     x     | 20        |            |
|  119  |   STO 2   | 44.02     |            |
|  120  |  RCL PV   | 45.13     |            |
|  121  |     +     | 40        |            |
|  122  |  STO PV   | 44.13     |            |
|  123  |   RCL 2   | 45.02     |            |
|  124  |   RCL 1   | 45.01     |            |
|  125  |   RCL 4   | 45.04     |            |
|  126  |     +     | 40        |            |
|  127  |   RCL 3   | 45.03     |            |
|  128  |     x     | 20        |            |
|  129  |     2     | 02        |            |
|  130  |     /     | 10        |            |
|  131  |   STO 1   | 44.01     |            |
|  132  |    R/S    | 31        |            |
|  133  |  GTO 003  | 43.33.003 |            |
|  134  |  RCL FV   | 45.15     | Prog. 004  |
|  135  |    CHS    | 16        |            |
|  136  |   RCL i   | 45.12     |            |
|  137  |     %     | 25        |            |
|  138  |  RCL PMT  | 45.14     |            |
|  139  |     +     | 40        |            |
|  140  |  RCL PV   | 45.13     |            |
|  141  |   RCL i   | 45.12     |            |
|  142  |     %     | 25        |            |
|  143  |  RCL PMT  | 45.14     |            |
|  144  |     +     | 40        |            |
|  145  |   x><y    | 34        |            |
|  146  |  R down   | 33        |            |
|  147  |     /     | 10        |            |
|  148  |    LN     | 43.23     |            |
|  149  |     1     | 01        |            |
|  150  |   RCL i   | 45.12     |            |
|  151  |     %     | 25        |            |
|  152  |     +     | 40        |            |
|  153  |    LN     | 43.23     |            |
|  154  |     /     | 10        |            |
|  155  |   STO n   | 44.11     |            |
|  156  |    R/S    | 31        |            |
|  157  |  GTO 004  | 43.33.004 |            |
|  158  |     1     | 01        | Prog. 005  |
|  159  |   x><y    | 34        |            |
|  160  |     %     | 25        |            |
|  161  |     +     | 40        |            |
|  162  |     1     | 01        |            |
|  163  |   RCL i   | 45.12     |            |
|  164  |     %     | 25        |            |
|  165  |     +     | 40        |            |
|  166  |   x><y    | 34        |            |
|  167  |     /     | 10        |            |
|  168  |     1     | 01        |            |
|  169  |     -     | 30        |            |
|  170  |    EEX    | 26        |            |
|  171  |     2     | 02        |            |
|  172  |     x     | 20        |            |
|  173  |   STO i   | 44.12     |            |
|  174  |    R/S    | 31        |            |
|  175  |  GTO 005  | 43.33.005 |            |
