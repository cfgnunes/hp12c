# Todos os programas instalados na HP 12c Platinum

A tabela a seguir apresenta todos os programas deste repositório instalados na memória RAM da calculadora HP 12c Platinum, que suporta até 399 linhas de código (em comparação com o limite de 99 linhas da versão padrão da HP 12c).

As linhas de 1 a 16 são reservadas para atalhos de acesso rápido a cada programa. Para acessar, por exemplo, o Programa 3, basta digitar `GTO 003` e pressionar `R/S`. Esse recurso elimina a necessidade de memorizar a linha inicial de cada programa, tornando o uso de múltiplos programas mais prático e eficiente.

Além disso, cada programa é configurado para retornar automaticamente à sua linha inicial após a execução. Assim, ao pressionar R/S após o término do Programa 3, por exemplo, ele será executado novamente. Esse recurso facilita a reexecução do programa selecionado.

A tabela abaixo inclui os programas:
- Programa 001 (início na linha 017): [Conversão entre taxas equivalentes](./01-taxas-equivalentes.md)
- Programa 002 (início na linha 037): [Sistema de Amortização Francês (SAF)](./01-taxas-equivalentes.md)
- Programa 003 (início na linha 096): [Sistema de Amortização Constante (SAC)](./03-tabela-sac.md)
- Programa 004 (início na linha 146): [Cálculo de prazo fracionário](./04-prazo-fracionario.md)
- Programa 005 (início na linha 174): [Cálculo de rentabilidade real](./05-rentabilidade-real.md)

| Linha | Instrução | Mostrador | Comentário |
| :---: | :-------: | --------- | ---------- |
|  001  |  GTO 017  | 43.33.017 |            |
|  002  |  GTO 037  | 43.33.037 |            |
|  003  |  GTO 096  | 43.33.096 |            |
|  004  |  GTO 146  | 43.33.146 |            |
|  005  |  GTO 174  | 43.33.174 |            |
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
|  017  |    x=0    | 43.35     | Prog. 001  |
|  018  |  GTO 035  | 43.33.035 |            |
|  019  |     1     | 01        |            |
|  020  |   RCL i   | 45.12     |            |
|  021  |     %     | 25        |            |
|  022  |     +     | 40        |            |
|  023  |   x><y    | 34        |            |
|  024  |   RCL n   | 45.11     |            |
|  025  |    x=0    | 43.35     |            |
|  026  |  GTO 035  | 43.33.035 |            |
|  027  |     /     | 10        |            |
|  028  |    y^x    | 21        |            |
|  029  |     1     | 01        |            |
|  030  |     -     | 30        |            |
|  031  |    EEX    | 26        |            |
|  032  |     2     | 02        |            |
|  033  |     x     | 20        |            |
|  034  |   STO i   | 44.12     |            |
|  035  |    R/S    | 31        |            |
|  036  |  GTO 001  | 43.33.001 |            |
|  037  |   STO 3   | 44.03     | Prog. 002  |
|  038  |     1     | 01        |            |
|  039  |   RCL i   | 45.12     |            |
|  040  |     %     | 25        |            |
|  041  |     +     | 40        |            |
|  042  |   RCL n   | 45.11     |            |
|  043  |    y^x    | 21        |            |
|  044  |   STO 4   | 44.04     |            |
|  045  |  RCL PV   | 45.13     |            |
|  046  |   STO 0   | 44.00     |            |
|  047  |   RCL i   | 45.12     |            |
|  048  |     %     | 25        |            |
|  049  |   RCL 4   | 45.04     |            |
|  050  |     x     | 20        |            |
|  051  |   RCL 4   | 45.04     |            |
|  052  |     1     | 01        |            |
|  053  |     -     | 30        |            |
|  054  |    x=0    | 43.35     |            |
|  055  |  GTO 094  | 43.33.094 |            |
|  056  |     /     | 10        |            |
|  057  |    CHS    | 16        |            |
|  058  |  STO PMT  | 44.14     |            |
|  059  |     1     | 01        |            |
|  060  |   RCL i   | 45.12     |            |
|  061  |     %     | 25        |            |
|  062  |     +     | 40        |            |
|  063  |   RCL 3   | 45.03     |            |
|  064  |    y^x    | 21        |            |
|  065  |   RCL 4   | 45.04     |            |
|  066  |   x><y    | 34        |            |
|  067  |     -     | 30        |            |
|  068  |   RCL 4   | 45.04     |            |
|  069  |     1     | 01        |            |
|  070  |     -     | 30        |            |
|  071  |    x=0    | 43.35     |            |
|  072  |  GTO 094  | 43.33.094 |            |
|  073  |     /     | 10        |            |
|  074  |   RCL 0   | 45.00     |            |
|  075  |     x     | 20        |            |
|  076  |  STO PV   | 44.13     |            |
|  077  |   RCL n   | 45.11     |            |
|  078  |   RCL 3   | 45.03     |            |
|  079  |     -     | 30        |            |
|  080  |   STO n   | 44.11     |            |
|  081  |   RCL 0   | 45.00     |            |
|  082  |    CHS    | 16        |            |
|  083  |  RCL PV   | 45.13     |            |
|  084  |     +     | 40        |            |
|  085  |   STO 2   | 44.02     |            |
|  086  |  RCL PMT  | 45.14     |            |
|  087  |   RCL 3   | 45.03     |            |
|  088  |     x     | 20        |            |
|  089  |   RCL 0   | 45.00     |            |
|  090  |  RCL PV   | 45.13     |            |
|  091  |     -     | 30        |            |
|  092  |     +     | 40        |            |
|  093  |   STO 1   | 44.01     |            |
|  094  |    R/S    | 31        |            |
|  095  |  GTO 002  | 43.33.002 |            |
|  096  |   STO 3   | 44.03     | Prog. 003  |
|  097  |  RCL PV   | 45.13     |            |
|  098  |   RCL i   | 45.12     |            |
|  099  |     %     | 25        |            |
|  100  |    CHS    | 16        |            |
|  101  |   STO 1   | 44.01     |            |
|  102  |  RCL PV   | 45.13     |            |
|  103  |   RCL n   | 45.11     |            |
|  104  |    x=0    | 43.35     |            |
|  105  |  GTO 144  | 43.33.144 |            |
|  106  |     /     | 10        |            |
|  107  |    CHS    | 16        |            |
|  108  |   STO 0   | 44.00     |            |
|  109  |   RCL i   | 45.12     |            |
|  110  |     %     | 25        |            |
|  111  |   RCL 3   | 45.03     |            |
|  112  |     1     | 01        |            |
|  113  |     -     | 30        |            |
|  114  |     x     | 20        |            |
|  115  |   RCL 1   | 45.01     |            |
|  116  |   x><y    | 34        |            |
|  117  |     -     | 30        |            |
|  118  |   STO 4   | 44.04     |            |
|  119  |   RCL 0   | 45.00     |            |
|  120  |     +     | 40        |            |
|  121  |  STO PMT  | 44.14     |            |
|  122  |   RCL n   | 45.11     |            |
|  123  |   RCL 3   | 45.03     |            |
|  124  |     -     | 30        |            |
|  125  |   STO n   | 44.11     |            |
|  126  |   RCL 0   | 45.00     |            |
|  127  |   RCL 3   | 45.03     |            |
|  128  |     x     | 20        |            |
|  129  |   STO 2   | 44.02     |            |
|  130  |  RCL PV   | 45.13     |            |
|  131  |     +     | 40        |            |
|  132  |  STO PV   | 44.13     |            |
|  133  |   RCL 2   | 45.02     |            |
|  134  |   RCL 1   | 45.01     |            |
|  135  |   RCL 4   | 45.04     |            |
|  136  |     +     | 40        |            |
|  137  |   RCL 3   | 45.03     |            |
|  138  |     x     | 20        |            |
|  139  |     2     | 02        |            |
|  140  |    x=0    | 43.35     |            |
|  141  |  GTO 144  | 43.33.144 |            |
|  142  |     /     | 10        |            |
|  143  |   STO 1   | 44.01     |            |
|  144  |    R/S    | 31        |            |
|  145  |  GTO 003  | 43.33.003 |            |
|  146  |  RCL FV   | 45.15     | Prog. 004  |
|  147  |    CHS    | 16        |            |
|  148  |   RCL i   | 45.12     |            |
|  149  |     %     | 25        |            |
|  150  |  RCL PMT  | 45.14     |            |
|  151  |     +     | 40        |            |
|  152  |  RCL PV   | 45.13     |            |
|  153  |   RCL i   | 45.12     |            |
|  154  |     %     | 25        |            |
|  155  |  RCL PMT  | 45.14     |            |
|  156  |     +     | 40        |            |
|  157  |   x><y    | 34        |            |
|  158  |  R down   | 33        |            |
|  159  |    x=0    | 43.35     |            |
|  160  |  GTO 172  | 43.33.172 |            |
|  161  |     /     | 10        |            |
|  162  |    LN     | 43.23     |            |
|  163  |     1     | 01        |            |
|  164  |   RCL i   | 45.12     |            |
|  165  |     %     | 25        |            |
|  166  |     +     | 40        |            |
|  167  |    LN     | 43.23     |            |
|  168  |    x=0    | 43.35     |            |
|  169  |  GTO 172  | 43.33.172 |            |
|  170  |     /     | 10        |            |
|  171  |   STO n   | 44.11     |            |
|  172  |    R/S    | 31        |            |
|  173  |  GTO 004  | 43.33.004 |            |
|  174  |     1     | 01        | Prog. 005  |
|  175  |   x><y    | 34        |            |
|  176  |     %     | 25        |            |
|  177  |     +     | 40        |            |
|  178  |     1     | 01        |            |
|  179  |   RCL i   | 45.12     |            |
|  180  |     %     | 25        |            |
|  181  |     +     | 40        |            |
|  182  |   x><y    | 34        |            |
|  183  |    x=0    | 43.35     |            |
|  184  |  GTO 192  | 43.33.192 |            |
|  185  |     /     | 10        |            |
|  186  |     1     | 01        |            |
|  187  |     -     | 30        |            |
|  188  |    EEX    | 26        |            |
|  189  |     2     | 02        |            |
|  190  |     x     | 20        |            |
|  191  |   STO i   | 44.12     |            |
|  192  |    R/S    | 31        |            |
|  193  |  GTO 005  | 43.33.005 |            |
