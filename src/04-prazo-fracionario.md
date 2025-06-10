# Cálculo de prazo fracionário

Este programa supre uma limitação conhecida da calculadora HP 12c, que realiza o cálculo do número de períodos (n) com base apenas em valores inteiros. Este programa permite obter o prazo fracionário, fornecendo o valor exato de n com casas decimais, o que é útil em análises financeiras que exigem precisão. O programa assume que os pagamentos periódicos (PMT) ocorrem no final de cada período (regime postecipado).

## Entradas e saídas do programa

**Entradas:**
- i = taxa de juros.
- PV = valor presente.
- PMT = pagamento periódico.
- FV = valor futuro.

**Saídas:**
- n e X = prazo calculado.

## Código do programa

| Linha | Instrução | Mostrador | Comentário                                   |
| :---: | :-------: | --------- | -------------------------------------------- |
|  01   |  RCL FV   | 45.15     |                                              |
|  02   |    CHS    | 16        |                                              |
|  03   |   RCL i   | 45.12     |                                              |
|  04   |     %     | 25        |                                              |
|  05   |  RCL PMT  | 45.14     |                                              |
|  06   |     +     | 40        |                                              |
|  07   |  RCL PV   | 45.13     |                                              |
|  08   |   RCL i   | 45.12     |                                              |
|  09   |     %     | 25        |                                              |
|  10   |  RCL PMT  | 45.14     |                                              |
|  11   |     +     | 40        |                                              |
|  12   |   x><y    | 34        |                                              |
|  13   |  R down   | 33        |                                              |
|  14   |    x=0    | 43.35     |                                              |
|  15   |  GTO 00   | 43.33.00  | Evita divisão por zero.                      |
|  16   |     /     | 10        |                                              |
|  17   |    LN     | 43.23     |                                              |
|  18   |     1     | 01        |                                              |
|  19   |   RCL i   | 45.12     |                                              |
|  20   |     %     | 25        |                                              |
|  21   |     +     | 40        |                                              |
|  22   |    LN     | 43.23     |                                              |
|  23   |    x=0    | 43.35     |                                              |
|  24   |  GTO 00   | 43.33.00  | Evita divisão por zero.                      |
|  25   |     /     | 10        |                                              |
|  26   |   STO n   | 44.11     | Armazena o prazo calculado no registrador n. |

## Fórmula utilizada no programa

$$
n = \frac{\ln\left(\frac{PMT + i \cdot FV}{PMT + i \cdot PV}\right)}{\ln(1 + i)}
$$

## Exemplos de utilização do programa

**Problema: Em quanto tempo uma taxa de juros mensal de 2,6% dobraria o seu patrimônio?**

Dados do problema:
- n = ?
- i = 2,6
- PV = -1
- PMT = 0
- FV = 2

Pressione as teclas:
```
2,6       [i]
1   [CHS] [PV]
2         [FV]
          [R/S]    (executa o programa)
```

O visor exibirá: 27,00 (meses para dobrar o patrimônio).

**Problema: Você investe R$ 3.000,00 e o valor dobra para R$ 6.000,00 com juros de 9% ao ano. Quanto tempo levou?**

Dados do problema:
- n = ?
- i = 9
- PV = -3.000
- PMT = 0
- FV = 6.000

Pressione as teclas:
```
9          [i]
3000 [CHS] [PV]
6000       [FV]
           [R/S]    (executa o programa)
```

Resposta: n = 8,04 (anos).
