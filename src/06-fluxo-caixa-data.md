# Inserção de fluxo de caixa com datas

Este programa transforma um fluxo de caixa com datas irregulares (CFj com datas e valores) em um fluxo de caixa equivalente com intervalos regulares baseado em dias, preenchendo os períodos sem entradas com fluxos de zero.

## Entradas e saídas do programa

**Entrada:** Fluxo de caixa irregular inserido uma data em CFj seguida do valor no próximo CFj.

**Saída:** Fluxo de caixa regular, baseado em dias, com zeros nos dias sem movimentação, preparado para análises com métodos que requerem intervalos regulares (funções NPV e IRR da calculadora).

## Código do programa

| Ordem | Instrução | Mostrador | Comentário                                                                      |
| :---: | :-------: | --------- | ------------------------------------------------------------------------------- |
|   1   |   RCL n   | 45.11     | Recupera a quantidade n de fluxos de caixa inseridos.                           |
|   2   |    x=0    | 43.35     | Verifica se n = 0.                                                              |
|   3   |  GTO 000  | 43.33.000 | Se n = 0, não há fluxo para processar, então finaliza.                          |
|   4   |  STO PMT  | 44.14     | Salva n no registrador PMT para restaurar mais tarde.                           |
|   5   |  RCL CFj  | 45.43.14  | Início do laço principal.                                                       |
|   6   |   RCL n   | 45.11     |                                                                                 |
|   7   |    x=0    | 43.35     | Se n = 0, terminou o laço principal.                                            |
|   8   |  GTO 043  | 43.33.043 | Vai para o fim do laço principal.                                               |
|   9   |     1     | 01        |                                                                                 |
|  10   |     -     | 30        |                                                                                 |
|  11   |   STO n   | 44.11     | n=n-1                                                                           |
|  12   |  R down   | 33        | Descarta o valor da pilha.                                                      |
|  13   |  RCL CFj  | 45.43.14  | Recupera a próxima data.                                                        |
|  14   |   x><y    | 34        | Reordena as datas para resultar em uma diferença positiva.                      |
|  15   |   ENTER   | 36        | Duplica a data na pilha para utilizar a verificação de data com o comando FRAC. |
|  16   |   FRAC    | 43.24     | Verifica se há parte decimal (indício de data válida).                          |
|  17   |    x=0    | 43.35     | Se FRAC retorna 0, não é uma data.                                              |
|  18   |  GTO 058  | 43.33.058 | Verificação de erro: se não for uma data, finaliza o programa com segurança.    |
|  19   |  R down   | 33        | Descarta o valor da pilha.                                                      |
|  20   |    DYS    | 43.26     | Calcula número de dias entre datas (intervalo).                                 |
|  21   |     1     | 01        |                                                                                 |
|  22   |     -     | 30        | Reduz 1 dia para converter em quantidade de lacunas.                            |
|  23   |   RCL n   | 45.11     |                                                                                 |
|  24   |     1     | 01        |                                                                                 |
|  25   |     +     | 40        |                                                                                 |
|  26   |   STO n   | 44.11     | n=n+1                                                                           |
|  27   |  R down   | 33        | Descarta o valor da pilha.                                                      |
|  28   |    Nj     | 43.15     | Salva intervalo (dias entre as datas) em Nj.                                    |
|  29   |   RCL n   | 45.11     |                                                                                 |
|  30   |     2     | 02        |                                                                                 |
|  31   |     +     | 40        |                                                                                 |
|  32   |   STO n   | 44.11     | n=n+2                                                                           |
|  33   |  RCL Nj   | 45.43.15  | Salva na pilha o valor de Nj para salvar após definir um CFj.                   |
|  34   |  RCL CFj  | 45.43.14  | Decrementa n.                                                                   |
|  35   |  R down   | 33        | Descarta o valor da pilha.                                                      |
|  36   |     0     | 00        |                                                                                 |
|  37   |    CFj    | 43.14     | CFj = 0 (para datas intermediárias).                                            |
|  38   |  R down   | 33        | Descarta o valor da pilha.                                                      |
|  39   |    Nj     | 43.15     | Salva novamente o valor de Nj (que é perdido após salvar o valor em CFj).       |
|  40   |  RCL CFj  | 45.43.14  | Decrementa n.                                                                   |
|  41   |  RCL CFj  | 45.43.14  | Decrementa n.                                                                   |
|  42   |  GTO 005  | 43.33.005 | Retorna ao laço principal.                                                      |
|  43   |     1     | 01        |                                                                                 |
|  44   |   STO n   | 44.11     | n=1.                                                                            |
|  45   |  RCL Nj   | 45.43.15  | Salva na pilha o valor de Nj para salvar após definir um CFj.                   |
|  46   |     0     | 00        |                                                                                 |
|  47   |   STO n   | 44.11     | n=0.                                                                            |
|  48   |    CFj    | 43.14     | CFj = 0 (para a primeira data).                                                 |
|  49   |  R down   | 33        | Descarta o valor da pilha.                                                      |
|  50   |    Nj     | 43.15     | Salva novamente o valor de Nj (que é perdido após salvar o valor em CFj).       |
|  51   |  RCL PMT  | 45.14     | Recupera n original.                                                            |
|  52   |     1     | 01        |                                                                                 |
|  53   |     -     | 30        |                                                                                 |
|  54   |   STO n   | 44.11     | Restaura n para valor original - 1.                                             |
|  55   |     0     | 00        |                                                                                 |
|  56   |  STO PMT  | 44.14     | Limpa PMT ao final.                                                             |
|  57   |  GTO 000  | 43.33.000 | Fim do programa.                                                                |
|  58   |  RCL PMT  | 45.14     | Subrotina de erro: recupera PMT.                                                |
|  59   |  GTO 054  | 43.33.054 | Vai para restauração final de n.                                                |

## Exemplos de utilização do programa

**Problema: Calcule a Taxa Interna de Retorno (TIR) para o fluxo de caixa abaixo:**

| Número | Data       | Valor (R$)                        |
| ------ | ---------- | --------------------------------- |
| 0      | 05/01/2007 | -10.000,00 (investimento inicial) |
| 1      | 04/02/2007 | 3.250,00                          |
| 2      | 06/03/2007 | 2.700,00                          |
| 3      | 05/04/2007 | 3.045,00                          |
| 4      | 05/05/2007 | 2.005,00                          |

Pressione as teclas:
```
               [g] [D.MY]
-10000   [CHS] [g] [CFo]    (CF0 = -10.000,00)
5.012007       [g] [CFj]    (data0 = 05/01/2007)
3250           [g] [CFj]    (CF1 = 3.250,00)
4.022007       [g] [CFj]    (data1 = 04/02/2007)
2700           [g] [CFj]    (CF2 = 2.700,00)
6.032007       [g] [CFj]    (data2 = 06/03/2007)
3045           [g] [CFj]    (CF3 = 3.045,00)
5.042007       [g] [CFj]    (data3 = 05/04/2007)
2005           [g] [CFj]    (CF4 = 2.005,00)
5.052007       [g] [CFj]    (data4 = 05/05/2007)
                   [R/S]    (executa o programa para converter o fluxo de caixa)
               [f] [IRR]    (calcula o TIR)
```

Resposta: TIR = 0,136933% ao dia.

Como alternativa, você poderia resolver este exercício sem o uso do programa, calculando a diferença em dias entre cada data e preenchendo as lacunas com fluxos de zero, embora isso exija mais trabalho. O processo seria o seguinte:

```
-10000   [CHS] [g] [CFo]    (CF0 = -10.000,00)
0              [g] [CFj]    (CF1 = 0)
29             [g] [Nj]     (29 dias entre 05/01/2007 e 04/02/2007)
3250           [g] [CFj]    (CF2 = 3.250,00)
0              [g] [CFj]    (CF3 = 0)
29             [g] [Nj]     (29 dias entre 04/02/2007 e 06/03/2007)
2700           [g] [CFj]    (CF4 = 2.700,00)
0              [g] [CFj]    (CF5 = 0)
29             [g] [Nj]     (29 dias entre 06/03/2007 e 05/04/2007)
3045           [g] [CFj]    (CF6 = 3.045,00)
0              [g] [CFj]    (CF7 = 0)
29             [g] [Nj]     (29 dias entre 05/04/2007 e 05/05/2007)
2005           [g] [CFj]    (CF8 = 2.005,00)
               [f] [IRR]    (calcula o TIR)
```
