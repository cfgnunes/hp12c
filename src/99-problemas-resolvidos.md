# Problemas resolvidos com a HP 12c

O objetivo destes exercícios é apresentar, de forma prática e aplicada, as principais funções da calculadora HP 12c. Ao resolver os problemas propostos, o usuário não apenas se familiariza com o uso da calculadora, mas também aprende, na prática, noções básicas do universo financeiro.

Antes de iniciar qualquer exercício envolvendo os registradores financeiros ou estatísticos, certifique-se de apagar os valores previamente armazenados na calculadora para evitar resultados incorretos. Para isso, pressione as teclas:
```
[f] [CLEAR REG]
```

Os registradores financeiros da calculadora HP 12c representam os principais elementos de uma operação financeira baseada no conceito de valor do dinheiro no tempo (*Time Value of Money* - TVM). São eles:
- **n**: número de períodos;
- **i**: taxa de juros por período;
- **PV (Present Value)**: valor presente (capital);
- **PMT (Payment)**: valor do pagamento periódico, utilizado em operações com séries de pagamentos;
- **FV (Future Value)**: valor futuro (montante), que representa o valor acumulado ao final dos períodos.

## Cálculos com porcentagem

**Problema: Em uma aplicação financeira, um investidor obteve um rendimento de R$ 10.000,00 sobre um capital total de R$ 250.000,00. Qual é o percentual que esse rendimento representa em relação ao valor investido?**

Pressione as teclas:
```
250 [ENTER]
10  [%T]
```

Resposta: 4% (percentual em relação ao total).

**Problema: Durante um período de valorização imobiliária, uma casa adquirida por R$ 200.000,00 foi vendida por R$ 220.000,00. Qual foi o percentual de aumento no valor da casa em relação ao valor de aquisição?**

Pressione as teclas:
```
200 [ENTER]
220 [Δ%]
```

Resposta: 10% (variação percentual).

**Problema: O preço de uma ação na bolsa de valores caiu de R$ 9,00 para R$ 8,00. Qual foi a variação percentual negativa (ou percentual de desvalorização) em relação ao preço inicial?**

Pressione as teclas:
```
9 [ENTER]
8 [Δ%]
```

Resposta: -11,11% (variação percentual).

**Problema: Em uma loja, um produto que custa R$ 400,00 está com um desconto de 15%. Qual é o valor correspondente a esse desconto? Calcule também o valor final já com o desconto.**

Pressione as teclas:
```
400 [ENTER]
15  [%]
```

O visor exibirá: 60,00 (valor do desconto).

Pressione a tecla: `[-]`

O visor exibirá: 340,00 (valor final do produto com o desconto).

**Problema: Uma cooperativa de alimentos compra caixas de sopa enlatada a um custo faturado de R$ 9,60 por caixa. Se a cooperativa utilizar rotineiramente uma margem de 15% sobre o custo, qual será o preço de venda de cada caixa de sopa?**

Pressione as teclas:
```
9,60 [ENTER]
15   [%]
     [+]
```

O visor exibirá: 11,04 (preço de venda).

## Cálculos com datas

**Problema: Se você comprasse uma opção para um terreno em 28 de maio de 2025, válida por 120 dias, qual seria a data de vencimento?**

Pressione as teclas:
```
          [g] [D.MY]
28,052025 [ENTER]
120       [g] [DATE]
```

O visor exibirá: 25.09.2025 4, representando a data de 25/09/2025. O número 4 exibido no visor indica o dia da semana (quinta-feira).

**Nota:** Na calculadora HP 12c, os dias da semana são numerados de 1 a 7, correspondendo 1 à segunda-feira e 7 ao domingo.

**Problema: Qual seria o número de dias entre 3 de junho de 2024 a 14 de outubro de 2025?**

Pressione as teclas:
```
          [g] [D.MY]
 3,062024 [ENTER]
14,102025 [g] [ΔDYS]
```

O visor exibirá: 498 (número exato de dias entre as datas)

Para saber o número de dias baseado no ano comercial (mês de 30 dias), basta pressionar a tecla `[x><y]`.

O visor exibirá: 491 (número de dias baseado no ano comercial)

**Problema: Hoje é 23 de outubro de 2024. O Sr. Carlos deseja agendar os próximos três encontros com seu cliente, respeitando um intervalo fixo de 21 dias entre cada reunião. Quais serão as datas desses encontros?**

Pressione as teclas:
```
          [g] [D.MY]
23,102024 [ENTER]
21        [g] [DATE]
```

O visor exibirá: 13.11.2024 (primeira data)

Para a próxima data, pressione as teclas:
```
[g] [LSTx]
[g] [DATE]
```

O visor exibirá: 4.12.2024 (segunda data)

Para a próxima data, pressione as teclas:
```
[g] [LSTx]
[g] [DATE]
```

O visor exibirá: 25.12.2024 (terceira data)

## Juros Simples

**Problema: Um capital de R$ 80.000,00 é aplicado à taxa de 30% ao ano, durante 90 dias. Utilizando o ano comercial de 360 dias, determine o valor dos juros simples acumulados no período e o montante total ao final da aplicação.**

Dados do problema:
- PV = -80.000
- i = 30% ao ano
- n = 90 dias

Pressione as teclas:
```
80000 [CHS] [PV]
30          [i]
90          [n]
            [f] [INT]    (cacula os juros simples)
```

O visor exibirá: 6.000,00 (valor dos juros simples acumulados).

Pressione a tecla: `[+]`

O visor exibirá: 86.000,00 (montante total ao final da aplicação).

**Problema: Você toma emprestado R$ 1.250,00 de um parente e concorda em devolver o dinheiro em um ano, com juro simples de 7%. Que importância você terá que pagar?**

Dados do problema:
- PV = 1.250
- i = 7% ao ano
- n = 360 dias

Pressione as teclas:
```
1250 [PV]
7    [i]
360  [n]
     [f] [INT]    (cacula os juros simples)
     [+]          (calcula o montante, soma os juros com o capital)
```

O visor exibirá: -1.337,50 (montante total que você terá que pagar).

**Problema: Você emprestou a um amigo que queria começar um novo negócio R$ 450,00 por 60 dias, cobrando juro anual simples de 7% (calculado na base de 365 dias). Quanto de juro ele estará lhe devendo em 60 dias e qual o montante total da dívida?**

Dados do problema:
- PV = -450
- i = 7% ao ano
- n = 60 dias

Pressione as teclas:
```
450 [CHS] [PV]
7   [i]
60  [n]
    [f] [INT]          (cacula os juros simples)
    [R down] [x><y]    (descarta o valor de juro na base de 360 dias)
```

O visor exibirá: 5,18 (quanto de juro ele estará lhe devendo).

Pressione a tecla: `[+]`

O visor exibirá: 455,18 (montante total da dívida).

## Pagamentos únicos: investimentos

**Problema: Você investe R$ 5.000,00 em uma conta que rende 6% ao ano durante 8 anos. Qual será o valor ao final do período?**

Dados do problema:
- n = 8
- i = 6
- PV = -5.000
- PMT = 0
- FV = ?

Pressione as teclas:
```
8          [n]
6          [i]
5000 [CHS] [PV]
           [FV]
```

Resposta: FV = 7.969,24

**Problema: Você precisa de R$ 10.000,00 em 5 anos. A conta rende 7% ao ano. Quanto deve investir agora?**

Dados do problema:
- n = 5
- i = 7
- PV = ?
- PMT = 0
- FV = 10.000

Pressione as teclas:
```
5     [n]
7     [i]
10000 [FV]
      [PV]
```

Resposta: PV = -7.129,86

**Problema: Você investe R$ 2.000,00 e o valor cresce para R$ 2.800 em 4 anos. Qual foi a taxa de juros anual?**

Dados do problema:
- n = 4
- i = ?
- PV = 2.000
- PMT = 0
- FV = 2.800

Pressione as teclas:
```
4    [n]
2000 [PV]
2800 [FV]
     [i]
```

Resposta: i = 8,78%

**Problema: Suponha que um título do governo pagará R$ 1.000,00 daqui a três anos. Se a taxa de juros dos títulos de 3 anos é de 4% ao ano, quanto vale esse título hoje?**

Dados do problema:
- n = 3
- i = 4
- PV = ?
- PMT = 0
- FV = 1.000

Pressione as teclas:
```
3    [n]
4    [i]
1000 [FV]
     [PV]
```

Resposta: PV = -889,00

**Problema: O Tesouro Nacional oferece um título por R$ 613,81. Nenhum pagamento será feito até o vencimento, em 10 anos, quando será resgatado por R$ 1.000,00. Qual a taxa de juros efetiva anual desse título?**

Dados do problema:
- n = 10
- i = ?
- PV = -613,81
- PMT = 0
- FV = 1.000

Pressione as teclas:
```
10           [n]
613,81 [CHS] [PV]
1000         [FV]
             [i]
```

Resposta: i = 5%

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
          [n]
```

O visor exibirá: 27,00 (meses para dobrar o patrimônio).

**Nota:** A calculadora HP 12c retorna o valor 28, em vez de 27,005 (valor exato), porque arredonda o resultado para cima em cálculos que envolvem a determinação do número de períodos (n). Ela obtém apenas valores inteiros para n, sendo uma limitação da calculadora. Para realizar o cálculo exato, utilize o programa [Cálculo de prazo fracionário](./04-prazo-fracionario.md).

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
           [n]
```

Resposta: n = 8,04 (anos).

**Nota:** A calculadora HP 12c retorna o valor 9, em vez de 8,04 (valor exato), porque arredonda o resultado para cima em cálculos que envolvem a determinação do número de períodos (n). Ela obtém apenas valores inteiros para n, sendo uma limitação da calculadora. Para realizar o cálculo exato, utilize o programa [Cálculo de prazo fracionário](./04-prazo-fracionario.md).

**Problema: Você deposita R$ 2.000,00 em uma conta de poupança que rende 7,2% de juros anuais, compostos anualmente. Se você não fizer nenhum outro depósito nesta conta, em quanto tempo você terá R$ 3.000,00?**

Dados do problema:
- n = ?
- i = 7,2
- PV = -2.000
- PMT = 0
- FV = 3.000

Pressione as teclas:
```
7,2        [i]
2000 [CHS] [PV]
3000       [FV]
           [n]
```

Resposta: n = 5,83 (anos)

**Nota:** A calculadora HP 12c retorna o valor 6, em vez de 5,83 (valor exato), porque arredonda o resultado para cima em cálculos que envolvem a determinação do número de períodos (n). Ela obtém apenas valores inteiros para n, sendo uma limitação da calculadora. Para realizar o cálculo exato, utilize o programa [Cálculo de prazo fracionário](./04-prazo-fracionario.md).

**Problema: Você aplica R$ 1.000,00 por 10 anos em um banco que paga 5% ao ano, com pagamento no final do período. Quanto terá ao final?**

Dados do problema:
- n = 10
- i = 5
- PV = -1.000
- PMT = 0
- FV = ?

Pressione as teclas:
```
10         [n]
5          [i]
1000 [CHS] [PV]
           [FV]
```

Resposta: FV = 1.628,89

**Problema: O Sr. Carlos pretende investir R$ 10.000,00 em uma aplicação com juros compostos de 8% ao ano, capitalizados trimestralmente. Qual será o valor futuro após 5 anos?**

Dados do problema:
- n = 5 x 4
- i = 8 / 4
- PV = -10.000
- PMT = 0
- FV = ?

Pressione as teclas:
```
5           [ENTER] 4 [x] [n]
8           [ENTER] 4 [/] [i]
10000 [CHS] [PV]
            [FV]
```

Resposta: FV = 14.859,47

**Problema: Quanto é preciso depositar hoje para ter R$ 8.000,00 em 5 anos, com juros de 6,5% ao ano capitalizados mensalmente?**

Dados do problema:
- n = 5 x 12
- i = 6,5 / 12
- PV = ?
- PMT = 0
- FV = 8.000

Pressione as teclas:
```
5    [g] [12x]
6,5  [g] [12/]
8000 [FV]
     [PV]
```

Resposta: PV = -5.785,29

**Problema: O Sr. Roberto vai se aposentar em 20 anos e quer comprar uma casa de R$ 2.000.000,00. Quanto ele precisa investir hoje em um banco que paga 9% ao ano com capitalização semestral?**

Dados do problema:
- n = 20 x 2
- i = 9 / 2
- PV = ?
- PMT = 0
- FV = 2.000.000

Pressione as teclas:
```
20      [ENTER] 2 [x] [n]
9       [ENTER] 2 [/] [i]
2000000 [FV]
        [PV]
```

Resposta: PV = -343.857,40

## Pagamentos únicos: empréstimos

**Problema: Você toma emprestado R$ 7.000,00 a uma taxa de 5% ao ano por 3 anos. Qual será o valor total a ser pago?**

Dados do problema:
- n = 3
- i = 5
- PV = -7.000
- PMT = 0
- FV = ?

Pressione as teclas:
```
3          [n]
5          [i]
7000 [CHS] [PV]
           [FV]
```

Resposta: FV = 8.103,38

**Problema: Você deve pagar R$ 10.000,00 em 6 anos. A taxa anual juros é de 4%. Quanto pode pegar emprestado hoje?**

Dados do problema:
- n = 6
- i = 4
- PV = ?
- PMT = 0
- FV = -10.000

Pressione as teclas:
```
6           [n]
4           [i]
10000 [CHS] [FV]
            [PV]
```

Resposta: PV = 7.903,15

**Problema: Você tomou R$ 1.500,00 emprestados e pagou R$ 1.800,00 após 2 anos. Qual foi a taxa de juros?**

Dados do problema:
- n = 2
- i = ?
- PV = 1.500
- PMT = 0
- FV = -1.800

Pressione as teclas:
```
2          [n]
1500       [PV]
1800 [CHS] [FV]
           [i]
```

Resposta: i = 9,54%

**Problema: Você tomou R$ 5.000,00 emprestados e pagou R$ 6.000,00 com juros anuais de 8%. Quanto tempo demorou?**

Dados do problema:
- n = ?
- i = 8
- PV = 5.000
- PMT = 0
- FV = -6.000

Pressione as teclas:
```
8          [i]
5000       [PV]
6000 [CHS] [FV]
           [n]
```

Resposta: n = 2,37 (anos).

**Nota:** A calculadora HP 12c retorna o valor 3, em vez de 2,37 (valor exato), porque arredonda o resultado para cima em cálculos que envolvem a determinação do número de períodos (n). Ela obtém apenas valores inteiros para n, sendo uma limitação da calculadora. Para realizar o cálculo exato, utilize o programa [Cálculo de prazo fracionário](./04-prazo-fracionario.md).

**Problema: Se João empresta R$ 1.500,00 a um amigo com taxa de 4,3% ao ano, capitalizada mensalmente, quanto de juros terá ao final de um ano?**

Dados do problema:
- n = 1 x 12
- i = 4,3 / 12
- PV = -1.500
- PMT = 0
- FV = ?

Pressione as teclas:
```
1          [g] [12x]
4,3        [g] [12/]
1500 [CHS] [PV]
           [FV]
           [RCL] [PV]
           [+]
```

Resposta:
Juros = 1.565,79 (FV) - 1.500,00 (PV) = 65,79

**Problema: Lucas pegou R$ 600,00 emprestados no banco e esse valor quadruplicou em 2 anos, com capitalização mensal. Qual foi a taxa de juros?**

Dados do problema:
- n = 2 x 12
- i = ?
- PV = -600
- PMT = 0
- FV = 2.400

Pressione as teclas:
```
2          [g] [12x]
600  [CHS] [PV]
2400       [FV]
           [i]
12         [x]
```

Resposta: i = 5,9463 x 12 = 71,36% (taxa anual capitalizada mensalmente)

**Problema: Uma empresa contrata um empréstimo no valor de R$ 50.000,00, com prazo de vencimento de 3,5 anos. Sabendo que a taxa de juros é de 22% ao ano, com capitalização anual, determine o montante a ser pago ao final do período.**

Dados do problema:
- n = 3,5
- i = 22
- PV = 50000
- PMT = 0
- FV = ?

**Nota:** Neste exercício, o período n é fracionário (ou seja, não é um número inteiro de anos). Nesse caso, é possível adotar duas convenções distintas para o cálculo dos juros compostos:
- Convenção linear: aplica-se juros compostos sobre a parte inteira do prazo, e juros simples sobre a fração restante.
- Convenção exponencial: aplica-se juros compostos sobre todo o período, incluindo tanto a parte inteira quanto a fracionária.

Resolvendo o problema com a convenção exponencial. Pressione as teclas:
```
      [STO] [EEX]    (pressionar até aparecer o símbolo 'C' no visor)
3,5   [n]
22    [i]
50000 [i]
      [FV]
```

Resposta: FV = -100.283,48

Resolvendo o problema com a convenção linear. Pressione as teclas:
```
      [STO] [EEX]    (pressionar até apagar o símbolo 'C' no visor)
3,5   [n]
22    [i]
50000 [i]
      [FV]
```

Resposta: FV = -100.779,56

## Anuidade[^1]: investimentos

**Problema: André deposita R$ 22.000,00 ao final de cada ano por 7 anos, em uma conta que rende 6% ao ano. Quanto ele terá ao final do período?**

Dados do problema:
- n = 7
- i = 6
- PV = 0
- PMT = -22.000
- FV = ?

Pressione as teclas:
```
7           [n]
6           [i]
22000 [CHS] [PMT]
            [FV]
```

Resposta: FV = 184.664,43

**Problema: Marcela deposita R$ 1.200,00 no final de cada trimestre por 10 anos, em uma conta que rende 8% ao ano com capitalização trimestral. Quanto terá ao final do período?**

Dados do problema:
- n = 10 x 4
- i = 8 / 4
- PV = 0
- PMT = -1.200
- FV = ?

Pressione as teclas:
```
10         [ENTER] 4 [x] [n]
8          [ENTER] 4 [/] [i]
1200 [CHS] [PMT]
           [FV]
```

Resposta: FV = 72.482,38

**Problema: Carlos quer se aposentar em 20 anos e, para isso, deposita R$ 200,00 no final de cada mês em um fundo que rende 7,2% ao ano com capitalização mensal. Quanto terá ao se aposentar?**

Dados do problema:
- n = 20 x 12
- i = 7,2 / 12
- PV = 0
- PMT = -200
- FV = ?

Pressione as teclas:
```
20        [g] [12x]
7,2       [g] [12/]
200 [CHS] [PMT]
          [FV]
```

Resposta: FV = 106.752,47

**Problema: Juliana quer se aposentar em 32 anos e planeja investir mensalmente em uma conta que rende 9% ao ano com capitalização mensal. Quanto precisa investir por mês para acumular R$ 2.000.000,00?**

Dados do problema:
- n = 32 x 12
- i = 9 / 12
- PV = 0
- PMT = ?
- FV = 2.000.000

Pressione as teclas:
```
32 [g] [12x]
9  [g] [12/]
2  [EEX] 6 [FV]
   [PMT]
```

Resposta: PMT = -902,32

**Problema: Com uma taxa de juros de 0,75% ao mês, quanto deve ser depositado mensalmente (no início do mês) para atingir R$ 100.000,00 em 5 anos?**

Dados do problema:
- n = 5 x 12
- i = 0,75
- PV = 0
- PMT = ?
- FV = 100.000

Pressione as teclas:
```
       [g] [BEG]    (pagamentos feitos no início dos períodos)
5      [g] [12x]
0,75   [i]
100000 [FV]
       [PMT]
```

Resposta: PMT = -1.315,97

**Problema: Com uma taxa de juros de 1% ao mês, quanto deve ser depositado mensalmente (no início do mês) para acumular R$ 1.000.000,00 em 20 anos?**

Dados do problema:
- n = 20 x 12
- i = 1
- PV = 0
- PMT = ?
- FV = 1.000.000

Pressione as teclas:
```
   [g] [BEG]    (pagamentos feitos no início dos períodos)
20 [g] [12x]
1  [i]
1  [EEX] 6 [FV]
   [PMT]
```

Resposta: PMT = -1.000,85

**Problema: Ricardo deposita R$ 500,00 no início de cada trimestre durante 7 anos, em uma conta com juros de 12% ao ano, capitalizados trimestralmente. Quanto ele terá ao final do período?**

Dados do problema:
- n = 7 x 4
- i = 12 / 4
- PV = 0
- PMT = -500
- FV = ?

Pressione as teclas:
```
          [g] [BEG]    (pagamentos feitos no início dos períodos)
7         [ENTER] 4 [x] [n]
12        [ENTER] 4 [/] [i]
500 [CHS] [PMT]
          [FV]
```

Resposta: FV = 22.109,43

**Problema: (Conta de Aposentadoria Tributada) Se você investir R$ 3.000,00 a cada ano, durante 35 anos, quanto você terá na conta ao aposentar-se? Suponha uma taxa de dividendo anual de 8,175% e a taxa de impostos de 28%, e que os pagamentos começam no dia de hoje. Qual será, em valores monetários de hoje, o poder aquisitivo de tal montante, admitindo-se um índice de inflação de 8% ao ano?**

Pressione as teclas:
```
      [g] [BEG]    (pagamentos feitos no início dos períodos)
3000  [CHS] [PMT]
35    [n]
8.175 [ENTER] 28 [%] [-] [i]
      [VF]
```

Resposta: VF = -345.505,61 (valor na conta ao aposentar-se)

Pressione as teclas:
```
0 [PMT]
8 [i]
  [PV]
```

Resposta: PV = -23.368,11 (poder aquisitivo de tal montante, admitindo-se um índice de inflação de 8% ao ano)

## Anuidade: empréstimos e financiamentos

**Problema: Determinado bem é vendido em 7 pagamentos mensais, iguais e consecutivos de R$ 4.000,00. Para uma taxa de juros de 2,6% a.m., até que preço compensa adquirir o aparelho a vista?**

Dados do problema:
- n = 7
- i = 2,6
- PV = ?
- PMT = -4.000
- FV = 0

Pressione as teclas:
```
7          [n]
4000 [CHS] [PMT]
2,6        [i]
           [PV]
```

Resposta: PV = 25,301,17 (compensa comprar até esse preço, comprando a vista)

**Problema: Um empréstimo de R$ 20.000,00 é concedido para pagamento em 5 prestações mensais, iguais e sucessivas de $ 4.300,00. Calcular o custo mensal deste empréstimo.**

Dados do problema:
- n = 5
- i = ?
- PV = 20.000
- PMT = -4.300
- FV = 0

Pressione as teclas:
```
20000       [PV]
5           [n]
4300  [CHS] [PMT]
            [i]
```

Resposta: i = 2,46% (ao mês).

**Problema: Você está comprando sua primeira casa por R$ 220.000,00 e pagará R$ 30.000,00 de entrada. Vai financiar os R$ 190.000,00 restantes em um empréstimo de 30 anos, com taxa nominal[^2] de 7% ao ano e parcelas fixas mensais (tabela Price). Qual será o valor das parcelas mensais?**

Dados do problema:
- n = 30 x 12
- i = 7 / 12
- PV = 190.000
- PMT = ?
- FV = 0

Pressione as teclas:
```
30  [g] [12x]
7   [g] [12/]
190 [EEX] 3 [PV]
    [PMT]
```

Resposta: PMT = -1.264,07

**Problema: Você quer comprar um carro de R$ 28.000,00. A concessionária oferece uma taxa de 4% ao ano, com capitalização mensal, para 48 meses. Quais serão as parcelas fixas mensais?**

Dados do problema:
- n = 48
- i = 4 / 12
- PV = 28.000
- PMT = ?
- FV = 0

Pressione as teclas:
```
48    [n]
4     [g] [12/]
28000 [PV]
      [PMT]
```

Resposta: PMT = -632,21

**Problema: Você está financiando a compra de um carro novo através de um empréstimo de 3 anos com juro anual de 10,5% ao ano, composto mensalmente. O preço à vista é R$ 7.250,00. Você dará uma entrada de R$ 1.500,00. Qual será o valor das prestações mensais? Que taxa de juro reduziria seu pagamento mensal em R$ 10,00?**

Dados do problema:
- n = 3 x 12
- i = 10,5 / 12
- PV = 7.250 - 1.500 (preço à vista descontando a entrada paga)
- PMT = ?
- FV = 0

Pressione as teclas:
```
3    [g] [12x]
10,5 [g] [12/]
7250 [ENTER] 1500 [-] [PV]
     [PMT]
```

Resposta: PMT = -186,89

Para calcular a taxa de juro que reduz o pagamento em  R$ 10,00, adicione 10 para reduzir o valor negativo de PMT.

Pressione as teclas:
```
10  [+] [PMT]
    [i]
12  [x]
```

Resposta: 6,75% (taxa nominal anual)

**Problema: Maria possui um empréstimo consignado, com 96 parcelas fixas (tabela Price) de R$ 1.340,00, das quais já pagou 13, restando um saldo devedor de R$ 42.458,51. Determine a taxa de juros anual com capitalização mensal e, em seguida, calcule quantas parcelas seriam eliminadas caso ela amortizasse R$ 1.000,00 hoje, utilizando amortização por tempo. Calcule também o novo valor da parcela caso ela optasse por realizar a amortização por valor da parcela.**

**Etapa 1:** Encontrar a taxa de juros.

Dados do problema:
- n = 83 (96 - 13)
- i = ?
- PV = 42.458,51
- PMT = -1.340,00
- FV = 0

Pressione as teclas:
```
96             [ENTER] 13 [-] [n]
42458,51       [PV]
1340     [CHS] [PMT]
               [i]
```

Resposta: i = 2,85% (taxa mensal)

**Etapa 2:** Encontrar a nova quantidade de parcelas (amortização por tempo).

Dados do problema:
- n = ?
- i = 2,85
- PV = 41.458,51 (retirado R$ 1.000,00 do saldo devedor de R$ 42.458,51)
- PMT = -1.340,00
- FV = 0

Pressione as teclas:
```
     [RCL] [PV]
1000 [-] [PV]
     [n]
```

O visor exibirá: n = 76. Logo, 83-76 = 7 parcelas eliminadas (amortização por tempo).

**Etapa 3:** Encontrar o novo valor da parcela (amortização por valor da parcela).

Dados do problema:
- n = 83 (96 - 13)
- i = 2,85
- PV = 41.458,51 (retirado R$ 1.000,00 do saldo devedor de R$ 42.458,51)
- PMT = ?
- FV = 0

Pressione as teclas:
```
96 [ENTER] 13 [-] [n]
[PMT]
```

Resposta: PMT = -1.308,48 (novo valor da parcela após amortização por parcela).

**Problema: Após uma consideração cuidadosa de suas finanças você decidiu que o pagamento máximo mensal que pode assumir é de R$ 630,00. Você pode dar uma entrada de R$ 12.000,00 e a taxa nominal de juro está fixada em 11,5% ao ano. Se você fizer um financiamento de 30 anos, qual será o valor máximo da compra que você poderá fazer?**

**Etapa 1:** Encontrar o valor presente desconsiderando a entrada de R$ 12.000,00.

Dados do problema:
- n = 30 x 12
- i = 11,5 / 12
- PV = ?
- PMT = -630,00
- FV = 0

Pressione as teclas:
```
30         [g] [12x]
11,5       [g] [12/]
630  [CHS] [PMT]
           [PV]
```

O visor exibirá: PV = 63.617,64

**Etapa 2:** Somar o valor de entrada R$ 12.000,00 ao valor presente.

Pressione as teclas:
```
63617,64 [ENTER]
12000,00 [+]
```

Resposta: R$ 75.617,64 (o valor máximo da compra que você poderá fazer)

## Anuidade: aposentadorias

**Problema: Você pode comprar uma anuidade que paga R$ 1.000,00 no final de cada ano por 5 anos. Se você pode ganhar 6% ao ano em outros investimentos de mesmo risco, qual o valor máximo que deve pagar?**

Dados do problema:
- n = 5
- i = 6
- PV = ?
- PMT = 1.000
- FV = 0

Pressione as teclas:
```
5    [n]
6    [i]
1000 [PMT]
     [PV]
```

Resposta: PV = -4.212,36

**Problema: Você herdou R$ 200.000,00 e investe a 6% ao ano. Quanto pode sacar no final de cada um dos próximos 15 anos?**

Dados do problema:
- n = 15
- i = 6
- PV = 200.000
- PMT = ?
- FV = 0

Pressione as teclas:
```
15     [n]
6      [i]
200000 [PV]
       [PMT]
```

Resposta: PMT = -20.592,55

## Arrendamento

**Problema: Um carro novo que custa R$ 13.500,00 pode ser adquirido através de um *leasing*[^11] de 3 anos, com a opção de compra ao final do período por R$ 7.500,00. Se a financeira quiser obter um rendimento anual nominal de 14%, qual deverá ser o valor dos pagamentos mensais, com um pagamento antecipado? Calcule o valor do pagamento sob o ponto de vista da financeira. Utilize o modo início (BEGIN), porque o primeiro pagamento é devido na assinatura do contrato.**

Dados do problema:
- n = 3 x 12
- i = 14 / 12
- PV = -13.500
- PMT = ?
- FV = 7.500

Pressione as teclas:
```
             [g] [BEG]    (pagamentos feitos no início dos períodos)
3            [g] [12x]
14           [g] [12/]
135000 [CHS] [PMT]
7500         [FV]
             [PMT]
```

Resposta: PMT = 289,19

## Anuidade com carência: financiamentos e empréstimos

**Problema: Um veículo pode ser comercializado em 36 prestações mensais de R$ 1.980,00 cada uma. Sabendo que a loja usa taxa de 1,45% ao mês e que há 1 mês de carência antes do pagamento da primeira prestação, encontre o valor à vista do veículo.**

Pressione as teclas:
```
0    [g] [CFj]    (CF1 = 0, mês de carência)
1980 [g] [CFj]    (CF2 = 1.980, parcelas)
36   [g] [Nj]     (indica que CF2 se repete 36 vezes)
1,45 [i]          (i = 1,45%)
     [f] [NPV]    (calcula o VPL)
```

Resposta: R$ 54.437,52

**Nota:** Observe neste exercício que é possível calcular o Valor Presente mesmo quando os valores dos pagamentos são diferentes, calculando o Valor Presente Líquido (VPL) por meio da análise do fluxo de caixa. Quando o investimento inicial (CFo) é igual a zero, o Valor Presente Líquido (VPL) será igual ao Valor Presente, pois VPL=VP-CFo.

**Problema: Um financiamento será quitado em 12 parcelas mensais fixas de R$ 200,00, com carência de 3 meses, ou seja, o pagamento da primeira parcela ocorre no quarto mês após a liberação do crédito. Considerando uma taxa de juros de 3,5% ao mês, determine o valor presente desse financiamento no momento da liberação dos recursos.**

Pressione as teclas:
```
0   [g] [CFj]    (CF1 = 0, mês de carência)
3   [g] [Nj]     (indica que CF1 se repete 3 vezes)
200 [g] [CFj]    (CF2 = 200, parcelas)
12  [g] [Nj]     (indica que CF2 se repete 12 vezes)
3,5 [i]          (i = 3,5%)
    [f] [NPV]    (calcula o VPL)
```

Resposta: R$ 1.743,15

**Problema: Um professor comprou um computador em uma loja especializada em 10 prestações mensais de R$ 100,00 cada uma, sendo a primeira prestação paga 4 meses após a compra. Por ser compra a prazo, a loja cobra taxa de 36% ao ano capitalizada mensalmente. Encontre o valor à vista do computador.**

Pressione as teclas:
```
0   [g] [CFj]    (CF1 = 0, mês de carência)
3   [g] [Nj]     (indica que CF1 se repete 3 vezes)
100 [g] [CFj]    (CF2 = 100, parcelas)
10  [g] [Nj]     (indica que CF2 se repete 10 vezes)
36  [g] [12/]    (i = 36/12)
    [f] [NPV]    (calcula o VPL)
```

Resposta: R$ 780,63

## Análise da decisão entre pagamento à vista e parcelado

**Problema: Pagar a vista ou parcelar? Você tem duas opções para adquirir um plano anual de academia: pagar à vista o valor total de R$ 1.560,00 ou parcelar em 12 vezes mensais de R$ 130,00 (sem juros na parcela). Considerando que você dispõe do valor total e tem a possibilidade de investi-lo em uma aplicação com rendimento de 0,7% ao mês, qual é a vantagem financeira (ou custo de oportunidade) de optar pelo parcelamento em vez do pagamento à vista?**

Dados do problema:
- n = 12
- i = 0,7
- PV = ?
- PMT = -130
- FV = 0

Pressione as teclas:
```
12        [n]
0,7       [i]
130 [CHS] [PMT]
          [PV]
```

O visor exibirá: 1491,28 (valor presente das parcelas)

Para saber a diferença entre o valor à vista e o valor presente das parcelas, pressione as teclas:
```
1560
[x><y] [-]
```

O visor exibirá: 68,72 (diferença entre o valor à vista e o valor presente das parcelas)

**Nota:** A diferença entre o valor à vista e o valor presente das parcelas representa o custo de oportunidade de pagar parcelado, ou seja, o quanto você perde financeiramente por não investir os R$ 1.560 à 9% ao ano).

**Problema: O vendedor de uma loja, vende um aparelho eletrônico com as seguintes condições: pagamento à vista de R$ 1,300.00 ou em 3 parcelas de R$ 456.00 (sem entrada). Qual é a taxa cobrada no parcelamento?**

Dados do problema:
- n = 3
- i = ?
- PV = 1300
- PMT = -456
- FV = 0

Pressione as teclas:
```
3          [n]
1300       [PV]
456  [CHS] [PMT]
           [i]
```

O visor exibirá: 2,59 (taxa mensal)

**Problema: Um veículo novo está sendo vendido por R$ 4.000,00 de entrada mais 6 pagamentos mensais, iguais e consecutivos de R$ 3.000,00. Sabendo-se que a taxa de juros de mercado é de 5,5% a.m., determinar até que preço interessa comprar o veículo a vista.**

Pressione as teclas:
```
4000 [g] [CFo]    (pagamento à vista, então já está no valor presente)
3000 [g] [CFj]    (CF1 = 3.000)
6    [g] [Nj]     (indica que CF1 se repete 6 vezes)
5,5  [i]          (i = 5,5%)
     [f] [NPV]    (calcula o VPL)
```

Resposta: R$ 18.986,59

## Análise de fluxo de caixa

**Problema: (Análise do VPL) Uma empresa está avaliando um projeto de instalação de painéis solares em uma fábrica de médio porte para reduzir os custos com eletricidade. O investimento inicial para o projeto é de R$ 500.000,00. A expectativa é que o projeto gere uma economia anual de R$ 120.000,00 em custos de energia durante os próximos 6 anos. Ao final do sexto ano, os painéis terão um valor residual de R$ 50.000,00 (valor de revenda ou sucata). A empresa definiu uma taxa mínima de atratividade (TMA) de 10% ao ano para esse tipo de projeto. Com base nas informações, calcule o Valor Presente Líquido (VPL) e diga se o investimento é viável.**

Pressione as teclas:
```
500000 [CHS] [g] [CFo]
120000       [g] [CFj]
6            [g] [Nj]
50000        [g] [CFj]
10           [i]
             [f] [NPV]
```

Resposta: VPL = 48.289,19

O VPL é positivo. Isso significa que o projeto é viável financeiramente, pois traz um retorno superior à taxa mínima exigida de 10% ao ano. A empresa pode prosseguir com o investimento.

**Problema: (Análise do VPL) O investidor Carlos está analisando a compra de um imóvel com 4 lojas comerciais, todas prontas para locação. O preço de compra do imóvel é de R$ 1.000.000,00. Carlos estima que conseguirá alugar cada loja por R$ 4.000,00 por mês, totalizando R$ 16.000,00 por mês, ou seja, R$ 192.000,00 por ano. Ele acredita que conseguirá manter a ocupação total por 10 anos, ao final dos quais planeja vender o imóvel por R$ 600.000,00. Carlos quer saber se esse investimento é viável financeiramente, considerando sua taxa mínima de atratividade (TMA) de 9% ao ano.**

Pressione as teclas:
```
1000000 [CHS] [g] [CFo]
192000        [g] [CFj]
10            [g] [Nj]
600000        [g] [CFj]
9             [i]
              [f] [NPV]
```

Resposta: VPL = 464.709,99

O VPL é positivo. Isso significa que o projeto é viável financeiramente, pois traz um retorno superior à taxa mínima exigida de 9% ao ano.

**Problema: (Cálculo de TIR) Determinar a Taxa Interna de Retorno (TIR) referente a um empréstimo de R$ 126.900,00 a ser liquidado em quatro pagamentos mensais e consecutivos de R$ 25.000,00, R$ 38.000,00, R$ 45.000,00 e R$ 27.000,00.**

Pressione as teclas:
```
126900       [g] [CFo]
25000  [CHS] [g] [CFj]
38000  [CHS] [g] [CFj]
45000  [CHS] [g] [CFj]
27000  [CHS] [g] [CFj]
             [f] [IRR]
```

Resposta: TIR = 2,47% ao mês.

**Problema: (Cálculo de TIR) Um empréstimo de R$ 5.000,00 será quitado em 4 parcelas mensais, conforme a tabela a seguir. Calcule a taxa de juros mensal equivalente aplicada nesse financiamento.**

| Mês | Valor da Parcela (R$) |
| --- | --------------------- |
| 1º  | 1.500,00              |
| 2º  | 1.600,00              |
| 3º  | 1.600,00              |
| 4º  | 1.700,00              |

Pressione as teclas:
```
5000 [CHS] [g] [CFo]    (CF0 = -5.000)
1500       [g] [CFj]    (CF1 = 1.500)
1600       [g] [CFj]    (CF2 = 1.600)
2          [g] [Nj]     (indica que CF2 se repete 2 vezes)
1700       [g] [CFj]    (CF3 = 1.700)
           [f] [IRR]    (calcula a TIR)
```

Resposta: 10,44% (taxa mensal)

**Problema: (Cálculo de TIR) Você recebeu uma oferta para investir R$ 20.000,00. O investimento oferece um retorno de pagamentos trimestrais durante quatro anos, conforme a tabela abaixo. Calcule a taxa anual nominal de retorno para este investimento.**

| Ano | Pagamentos | Valor por Pagamento |
| --- | ---------- | ------------------- |
| 1   | 4          | R$ 500,00           |
| 2   | 4          | R$ 1.000,00         |
| 3   | 4          | R$ 2.000,00         |
| 4   | 4          | R$ 3.000,00         |

Pressione as teclas:
```
20000 [CHS] [g] [CFo]    (CF0 = -20.000)
500         [g] [CFj]    (CF1 = 500)
4           [g] [Nj]     (indica que CF1 se repete 4 vezes)
1000        [g] [CFj]    (CF2 = 1.000)
4           [g] [Nj]     (indica que CF2 se repete 4 vezes)
2000        [g] [CFj]    (CF3 = 2.000)
4           [g] [Nj]     (indica que CF3 se repete 4 vezes)
3000        [g] [CFj]    (CF4 = 3.000)
4           [g] [Nj]     (indica que CF4 se repete 4 vezes)
            [f] [IRR]    (calcula a TIR)
```

Resposta TIR = 2,43% (taxa trimestral) x 4 = 9,72% (taxa anual)

**Problema: (Cálculo de VPL, TIR e Payback) Você está avaliando a compra de um equipamento no valor de R$ 100.000,00 para aumentar a produção da sua empresa. Esse investimento promete um retorno anual de R$ 18.000,00 por 10 anos. Com base nessas informações, calcule o Valor Presente Líquido (VPL), a Taxa Interna de Retorno (TIR) e o *Payback* Simples[^3] (tempo necessário para recuperar o valor investido sem considerar o valor do dinheiro no tempo). A empresa considera o custo de oportunidade ou retorno requirido de 10% ao ano.**

Encontrando o Valor Presente Líquido (VPL). Pressione as teclas:
```
100000 [CHS] [g] [CFo]    (CF0 = -100.000)
18000        [g] [CFj]    (CF1 = 18.000)
10           [g] [CFj]    (indica que CF1 se repete 10 vezes)
10           [i]          (i = 10%)
             [f] [NPV]    (calcula o VPL)
```

Resposta: R$ 10.602,21 (valor presente líquido)

Encontrando a Taxa Interna de Retorno (TIR). Pressione as teclas:
```
[f] [IRR]
```

Resposta: 12,41% (valor presente líquido)

Para calcular o *Payback* Simples, basta somar os fluxos de caixa anuais até que o total acumulado iguale ou ultrapasse o valor do investimento inicial.
No caso de fluxos de caixa constantes (iguais a cada período), o cálculo pode ser simplificado dividindo o valor investido por um único fluxo de caixa.

```
100000 [ENTER]
18000  [/]
```

Resposta: 5,56 (anos para recuperar o valor investido)

**Problema: (Cálculo de TIR com datas) José depositou R$ 50.000,00 em sua conta no dia 1º de maio de 2005 e mais R$ 40.000,00 no dia 1º de julho de 2005. A carteira também recebeu e reinvestiu dividendos de R$ 30.000,00 no dia 1º de julho, além de mais R$ 30.000,00 em 31 de dezembro. Sua conta possuía valores (incluindo dividendos e aportes) de R$ 2.375.000,00 e R$ 2.460.000,00 em 1º de maio e 1º de julho, respectivamente. A conta foi avaliada em R$ 2.225.000,00 em 1º de janeiro de 2005 e em R$ 2.445.000,00 em 31 de dezembro de 2005. Qual é a taxa interna de retorno mensal?**

Primeiro, devemos identificar as informações importantes, ou seja, os fluxos de caixa que devem ser considerados no cálculo da taxa interna de retorno (TIR):

- 01/01/2005: Valor inicial da carteira: R$ 2.225.000,00
- 01/05/2005: Aporte de R$ 50.000,00
- 01/07/2005: Aporte de R$ 40.000,00
- 31/12/2005: Valor final da carteira: R$ 2.445.000,00

Os dividendos recebidos podem ser ignorados, pois foram reinvestidos, ou seja, permaneceram na carteira e não são entradas ou saídas externas de dinheiro. Se não tivessem sido reinvestidos, deveriam ser tratados como saques. Também podemos desconsiderar outras avaliações intermediárias, porque, no cálculo da TIR, só precisamos do valor inicial, dos aportes e do valor final.

Para usar a calculadora financeira, os fluxos de caixa devem estar espaçados regularmente. Os meses sem fluxo de caixa recebem valor zero: 01/02, 01/03, 01/04, 01/08, 01/09, 01/10, 01/11 e 01/12. Por aproximação, pode-se considerar que o valor final da carteira foi obtido em 01/01/2006 (em vez de 31/12/2005).

Pressione as teclas:
```
2225000 [CHS] [g] [CF0]    (CF0 = -2.225.000)
0             [g] [CFj]    (CF1 = 0)
3             [g] [Nj]     (indica que CF1 se repete 3 vezes)
50000   [CHS] [g] [CFj]    (CF2 = -50.000)
0             [g] [CFj]    (CF3 = 0)
40000   [CHS] [g] [CFj]    (CF4 = -40.000)
0             [g] [CFj]    (CF5 = 0)
5             [g] [Nj]     (indica que CF5 se repete 5 vezes)
2445000       [g] [CFj]    (CF6 = 2.445.000)
              [f] [IRR]    (calcula a TIR)
```

Resposta: TIR = 0,47% (taxa interna de retorno mensal)

**Problema: (Valor futuro com pagamentos irregulares) Um investidor realiza 5 depósitos mensais consecutivos em uma aplicação financeira que rende 1% ao mês, com capitalização mensal. Cada pagamento é feito ao final de cada mês conforme os dados abaixo. Calcule o valor futuro total acumulado ao final do período, após o último depósito.**

| Mês | Depósitos (R$) |
| --- | -------------- |
| 1   | 500,00         |
| 2   | 700,00         |
| 3   | 600,00         |
| 4   | 200,00         |
| 5   | 200,00         |

**Nota:** Na HP 12c, como não há uma função específica para calcular o valor futuro (VF) de fluxos de caixa irregulares, a solução é primeiro obter o valor presente (VP) usando a função NPV (para fluxos com valores distintos) e, em seguida, converter esse VP em VF tratando-o como um único pagamento e aplicando a taxa de juros e o prazo desejados.

Pressione as teclas:
```
500 [CHS] [g] [CFj]
700 [CHS] [g] [CFj]
600 [CHS] [g] [CFj]
200 [CHS] [g] [CFj]
2         [g] [Nj]
1         [i]
          [f] [NPV]
5         [n]
          [FV]
```

Resposta: R$ 2.035,22

**Uma empresa avalia um investimento de R$ 20.000,00 que gera os seguintes fluxos de caixa ao longo de 4 anos, com uma taxa mínima de atratividade de 10% ao ano, e deseja saber qual é a Série Uniforme Líquida[^4] (*Net Uniform Series*) equivalente.**

| Ano | Fluxo de Caixa (R$) |
| --- | ------------------- |
| 1   | 5.000,00            |
| 2   | 6.000,00            |
| 3   | 7.000,00            |
| 4   | 8.000,00            |

**Nota:** Na HP 12c, não há uma função direta para calcular a Série Uniforme Líquida a partir de fluxos de caixa não uniformes. Para isso, deve-se inicialmente calcular o Valor Presente Líquido (VPL) utilizando a função de fluxo de caixa. Em seguida, esse valor presente deve ser convertido em uma série uniforme equivalente por meio do cálculo do PMT, tratando o problema como uma operação de valor do dinheiro no tempo (TVM), com os mesmos prazo e taxa de juros utilizados no cálculo do VPL.

Pressione as teclas:
```
20000 [CHS] [g] [CFj]
5000        [g] [CFj]
6000        [g] [CFj]
7000        [g] [CFj]
8000        [g] [CFj]
10          [i]
            [f] [NPV]
4           [n]
            [PMT]
```

Resposta: R$ 71,75

## Cálculo de depreciação

**Problema: Uma clínica médica adquiriu um aparelho de ultrassom por R$ 120.000,00, com vida útil estimada de 6 anos e valor de sucata de R$ 12.000,00. Deseja-se calcular, utilizando o método linear de depreciação, o valor da depreciação anual e o valor estimado do equipamento ao final do quarto ano de uso.**

Pressione as teclas:
```
120000 [PV]
12000  [FV]
6      [n]
4      [f] [DEPREC. SL]
```

O visor exibirá: R$ 18.000,00 (depreciação correspondente ao terceiro ano).

Pressione as teclas:
```
[x><y]
[RCL] [FV]
[+]
```

O visor exibirá: R$ 48.000,00 (valor estimado do bem ao final do terceiro ano).

**Problema: Uma empresa adquiriu um veículo de entrega por R$ 100.000,00 com vida útil estimada de 8 anos e valor residual de R$ 40.000,00. Deseja-se calcular, utilizando o método da soma dos dígitos dos anos, o valor da depreciação correspondente ao terceiro ano de uso, bem como o valor de revenda do veículo ao final desse ano.**

Pressione as teclas:
```
100000 [PV]
40000  [FV]
8      [n]
3      [f] [DEPREC. SOYD]
```

O visor exibirá: R$ 10.000,00 (depreciação correspondente ao terceiro ano).

Pressione as teclas:
```
[x><y]
[RCL] [FV]
[+]
```

O visor exibirá: R$ 65.000,00 (valor de revenda do veículo ao final desse ano).

**Problema: Uma câmera cinematográfica comprada por R$ 12.000,00 tem uma vida útil de 10 anos com um valor residual de R$ 500,00. Utilizando o método da soma dos dígitos dos anos, calcule o valor da depreciação para o quarto ano.**

**Etapa 1:** Encontrar a depreciação do quarto ano.

Pressione as teclas:
```
12000 [PV]
500   [FV]
10    [n]
4     [f] [DEPREC. SOYD]
```

O visor exibirá: R$ 1.463,64 (depreciação no quarto ano).

**Problema: Uma máquina para trabalhar metal, comprada por R$ 10.000, é depreciada durante 5 anos. Seu valor de revenda após vida útil é estimado em R$ 500. Calcule a depreciação e o valor residual no terceiro ano da vida útil da máquina usando o método de saldos decrescentes com o dobro da taxa linear (um saldo decrescente de 200%).**

**Nota:** O valor residual é o valor contábil menos o valor de revenda após vida útil (valor de sucata).

Pressione as teclas:
```
10000 [PV]
500   [FV]
5     [n]
200   [i]
2     [f] [DEPREC. DB]
```

O visor exibirá: R$ 1.440,00 (depreciação no terceiro ano).

Pressione a tecla: `[x><y]`

O visor exibirá: R$ 1.660,00 (valor residual depois do terceiro ano).

## Cálculos estatísticos

**Problema: (Estatística descritiva) Você decidiu analisar seus gastos mensais com supermercado para entender melhor seus hábitos de consumo e planejar melhor seu orçamento. Durante quatro meses, você anotou o quanto gastou em cada visita ao supermercado. Com base nos dados a seguir, calcule o gasto médio mensal com supermercado:**

| Mês | Gasto (R$) |
| --- | ---------- |
| 1   | 215,40     |
| 2   | 198,75     |
| 3   | 230,10     |
| 4   | 205,80     |

Pressione as teclas:
```
215,40 [Σ+]
198,75 [Σ+]
230,10 [Σ+]
205,80 [Σ+]
       [g] [x̄]
```

Resposta: R$ 212,51 (valor médio)

**Problema: (Estatística descritiva) Você decide analisar o comportamento de duas ações da bolsa de valores. Seu objetivo é comparar a média dos preços e a volatilidade (medida pelo desvio padrão[^5]) dessas ações em um período recente. Qual das duas apresentou maior variação de preço e qual foi o preço médio de cada ação nesse período?**

| Semana | Ação Y | Ação X |
| ------ | ------ | ------ |
| 1      | 28,50  | 65,10  |
| 2      | 29,10  | 66,80  |
| 3      | 27,80  | 64,90  |
| 4      | 28,20  | 67,50  |

Pressione as teclas:
```
28,50 [ENTER] 65,10 [Σ+]
29,10 [ENTER] 66,80 [Σ+]
27,80 [ENTER] 64,90 [Σ+]
28,20 [ENTER] 67,50 [Σ+]
[g] [s]
```

O visor exibirá: 1,28 (desvio padrão amostral da Ação X)

Pressione a tecla: `[x><y]`

O visor exibirá: 0,55 (desvio padrão amostral da Ação Y)

Resposta: A ação X apresentou maior variação de preço, comparada à ação Y.

Agora, para obter as médias, pressione as teclas: `[g] [x̄]`

O visor exibirá: 66,08 (preço médio da Ação X)

Pressione a tecla: `[x><y]`

O visor exibirá: 28,40 (preço médio da Ação Y)

**Problema: (Regressão linear) Você deseja entender como sua renda mensal influencia o valor que consegue poupar ao final de cada mês. Nos últimos meses, registrou sua renda mensal e o valor correspondente economizado no período. Com base nesses dados, utilize um modelo de regressão linear simples para prever quanto conseguirá poupar caso sua renda seja de R$ 4.000,00. Estime também qual deveria ser sua renda para alcançar uma poupança de R$ 800,00.**

| Renda (R$) | Poupança (R$) |
| ---------- | ------------- |
| 3.200,00   | 420,00        |
| 3.450,00   | 480,00        |
| 3.100,00   | 390,00        |
| 3.600,00   | 520,00        |

Pressione as teclas:
```
3200 [ENTER] 420 [Σ+]
3450 [ENTER] 480 [Σ+]
3100 [ENTER] 390 [Σ+]
3600 [ENTER] 520 [Σ+]
4000 [g] [x̂,r]
```

O visor exibirá: 622,15 (poupança estimada caso a renda seja de R$ 4.000,00).

Pressione as teclas: `800 [g] [ŷ,r]`

O visor exibirá: 4.694,53 (renda estimada para obter um poupança de R$ 800,00).

Para visualizar o valor do coeficiente de correlação[^6], basta pressionar a tecla `[x><y]`.

**Problema: (Média ponderada) João realizou três compras de ações de uma mesma empresa na bolsa de valores, em momentos diferentes, com preços e quantidades distintas. Agora, ele deseja saber qual foi o preço médio de aquisição das ações, para uma possível venda futura. Desconsidere outras possíveis taxas.**

A tabela abaixo resume as compras feitas:

| Preço (R$) | Quantidade |
| ---------- | ---------- |
| 15,00      | 200        |
| 18,00      | 150        |
| 16,50      | 250        |

Pressione as teclas:
```
15,00 [ENTER] 200 [Σ+]
18,00 [ENTER] 150 [Σ+]
16,50 [ENTER] 250 [Σ+]
      [g] [x̄ w]
```

O visor exibirá: 16,38 (preço médio).

**Problema: (Média ponderada) Uma pesquisa de preço de aluguel de 266 apartamentos de um quarto revelou que 54 estavam alugados por R$ 200,00 por mês, 32 por R$ 205,00, 88 por R$ 210,00 e 92 por R$ 216,00. Qual é a media de aluguel mensal?**

Pressione as teclas:
```
200 [ENTER] 54 [Σ+]
205 [ENTER] 32 [Σ+]
210 [ENTER] 88 [Σ+]
216 [ENTER] 92 [Σ+]
    [g] [x̄ w]
```

O visor exibirá: 209,44 (aluguel médio mensal).

## Taxas equivalentes

**Nota:** Para os exercícios a seguir, utilize o programa [Conversão entre taxas equivalentes](./01-taxas-equivalentes.md).

**Problema: Você possui uma taxa de 1% ao mês e deseja saber qual é a taxa anual equivalente.**

Pressione as teclas:
```
1  [i]
1  [n]      (1 mês: período mensal)
12          (12 meses: período anual)
   [R/S]    (executa o programa)
```

O visor exibirá: 12,68 (taxa equivalente anual).

**Problema: Você possui uma taxa de 12% ao ano e deseja saber qual é a taxa mensal equivalente.**

Pressione as teclas:
```
12 [i]
12 [n]      (12 meses: período anual)
1           (1 mês: período mensal)
   [R/S]    (executa o programa)
```

O visor exibirá: 0,95 (taxa equivalente mensal).

**Problema: Quais as taxas de juros compostos mensal e trimestral equivalentes a 25% ao ano?**

Pressione as teclas:
```
25 [i]
12 [n]      (12 meses: período anual)
1           (1 mês: período mensal)
   [R/S]    (executa o programa)
```

O visor exibirá: 1,88 (taxas de juros anual, capitalizada mensalmente).

Pressione as teclas:
```
25 [i]
12 [n]      (12 meses: período anual)
3           (3 meses: período trimestral)
   [R/S]    (executa o programa)
```

O visor exibirá: 5,74 (taxas de juros anual, capitalizada mensalmente).

**Problema: Um aplicação financeira promete pagar 42% ao ano de juros. Sendo de um mês o prazo da aplicação, pede-se determinar a sua rentabilidade efetiva considerando os juros de 42% a. a. como taxa efetiva e taxa nominal.**

Considerando 42% a.a. como taxa efetiva, pressione as teclas:
```
42 [i]
12 [n]      (12 meses: período anual)
1           (1 mês: período mensal)
   [R/S]    (executa o programa)
```

O visor exibirá: 2,97 (taxa ao mês).

Considerando 42% a.a. como taxa nominal, pressione as teclas:
```
42 [ENTER]
12 [/]
```

O visor exibirá: 2,97 (taxa ao mês).

**Problema: Você considera abrir uma conta de poupança em um destes três bancos. Qual deles lhe oferece a melhor taxa de juros?**

| Banco | Juros anuais (%) | Tipo de composição                    |
| ----- | ---------------- | ------------------------------------- |
| A     | 6,70%            | Trimestral                            |
| B     | 6,65%            | Mensal                                |
| C     | 6,65%            | Contínua[^7] (capitalização contínua) |

Para obter a taxa efetiva anual do Banco A, pressione as teclas:
```
6,70 [ENTER] 4 [/] [i] (converte a taxa nominal para taxa efetiva trimestral)
3    [n]               (3 meses: período trimestral)
12                     (12 meses: período anual)
     [R/S]             (executa o programa)
```

O visor exibirá: 6,87 (taxa efetiva anual do Banco A).

Para obter a taxa efetiva anual do Banco B, pressione as teclas:
```
6,65 [ENTER] 12 [/] [i] (converte a taxa nominal para taxa efetiva mensal)
1    [n]                (1 mês: período mensal)
12                      (12 meses: período anual)
     [R/S]              (executa o programa)
```

O visor exibirá: 6,86 (taxa efetiva anual do Banco B).

Para obter a taxa efetiva anual do Banco C, pressione as teclas:
```
1    [ENTER]
6,65 [%]
     [e^x]
1    [-]
100  [x]
```

O visor exibirá: 6,88 (taxa efetiva anual do Banco C).

Os cálculos mostram que o Banco C oferece a taxa mais favorável (maior taxa).

## Taxa real

**Nota:** Para os exercícios a seguir, utilize o programa [Cálculo de rentabilidade real](./05-rentabilidade-real.md).

**Problema: Determinar a variação real do poder aquisitivo de um assalariado que obtém, em determinado semestre, um reajuste salarial de 12%, admitindo que a inflação do período tenha atingido a 8%.**

```
12 [i]
8  [R/S]    (executa o programa)
```

Resposta: 3,7% (variação real).

**Problema: Um banco informou que a rentabilidade de um determinado investimento foi de 12% ao ano, correspondendo aos juros nominais. No mesmo período, a inflação acumulada foi de 5%. Calcule os juros reais, ou seja, a rentabilidade efetiva do investimento descontando-se a inflação.**

Pressione as teclas:
```
12 [i]
5
   [R/S]    (executa o programa)
```

Resposta: 6,67% (taxa real de juros).

## Financiamentos e empréstimos com o Sistema de Amortização Francês (SAF) - Tabela Price

**Problema: Qual é o pagamento mensal necessário para amortizar completamente uma hipoteca no valor de R$ 30.000,00, por um prazo de 30 anos, se a taxa nominal de juro é de 12%?**

Dados do problema:
- n = 30 x 12
- i = 12 / 12
- PV = 30.000
- PMT = ?
- FV = 0

Pressione as teclas:
```
30    [g] [12x]
12    [g] [12/]
30000 [PV]
      [PMT]        (encontra o valor das parcelas fixas)
```

Resposta: PMT = -308,58 (valor das parcelas fixas).

**Problema: Você assumiu, na compra de uma casa, uma hipoteca[^8] de 25 anos de R$ 75.250,00 com juros nominais de 13,8% ao ano. Você estima morar na casa por 4 anos e depois vendê-la, liquidando o empréstimo. Qual será o valor da liquidação ao final de quatro anos? (considere as parcelas fixas, usando o sistema de amortização francês)**

**Nota:** Este problema consiste em encontrar o saldo devedor após 4 anos (48 meses) de financiamento.

Pressione as teclas:
```
25    [g] [12x]
13,8  [g] [12/]
75250 [PV]
      [PMT]          (encontra o valor das parcelas fixas)
48    [f] [AMORT]    (amortização de 48 meses)
      [RCL] [PV]     (exibe o saldo devedor)
```

Resposta: R$ 73.408,83 (valor da liquidação ao final de quatro anos, saldo devedor)

**Nota:** Como alternativa, você pode usar o programa [Sistema de Amortização Francês (SAF) - Tabela Price](./02-tabela-price.md). Diferentemente da função AMORT da HP 12c, este programa calcula o valor exato sem realizar iterações, evitando erros de arredondamento. Além disso, não é necessário informar o valor das parcelas (PMT). Confira o procedimento a seguir:

Pressione as teclas:
```
25    [g] [12x]
13,8  [g] [12/]
75250 [PV]
48                   (amortização de 48 meses)
      [R/S]          (executa o programa)
      [RCL] [PV]     (exibe o saldo devedor)
```

Resposta: R$ 73.408,78 (valor da liquidação ao final de quatro anos, saldo devedor)

## Financiamentos e empréstimos com o Sistema de Amortização Constante (SAC)

**Nota:** Para os exercícios a seguir, utilize o programa [Sistema de Amortização Constante (SAC)](./03-tabela-sac.md).

**Problema: Considere um empréstimo de R$ 500.000,00, com taxa de juros de 2% ao mês e prazo total de 20 meses. Com base nessas condições, calcule o total de juros pagos até a 13ª parcela, bem como o valor total pago até essa mesma parcela. Considere o Sistema de Amortização Constante (SAC).**

Pressione as teclas:
```
500000 [PV]
2      [i]
20     [n]
13
       [R/S]    (executa o programa)
```

O visor exibirá: -91.000,00 (total de juros pagos até a 13ª parcela).

Pressione a tecla: `[+]`

O visor exibirá: -416.000,00 (total pago até a 13ª parcela).

**Problema: Considere um empréstimo no valor de R$350.000,00, com taxa de juros de 1% ao mês e prazo de 35 meses. Com base nesses dados, determine os juros pagos especificamente na 28ª parcela, bem como o valor total dessa parcela. Considere o Sistema de Amortização Constante (SAC).**

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

O visor exibirá: -800,00 (juros pagos somente na 28ª parcela).

Pressione as teclas:
```
[RCL] [PMT]
```

O visor exibirá: -10.800,00 (valor da 28ª parcela).

**Problema: Considere um empréstimo no valor de R$ 320.000,00, com taxa de juros de 3% ao mês e prazo total de 42 meses. Com base nessas condições, calcule o total de juros pagos ao longo de todo o financiamento, assim como o valor total desembolsado com o pagamento das parcelas durante todo o período. Considere o Sistema de Amortização Constante (SAC).**

Pressione as teclas:
```
320000 [PV]
3      [i]
42     [n]
42
       [R/S]    (executa o programa)
```

O visor exibirá: -206.400,00 (total de juros pagos durante todo o financiamento).

Pressione a tecla: `[+]`

O visor exibirá: -526.400,00 (total pago em parcelas ao longo de todo o financiamento).

**Problema: Considere um empréstimo no valor de R$260.000,00, com taxa de juros de 4% ao mês e prazo total de 38 meses. Com base nessas condições, calcule, para o período entre a 16ª e a 27ª parcela: o total de juros pagos, o total de amortizações realizadas e o valor total desembolsado com o pagamento dessas parcelas. Considere o Sistema de Amortização Constante (SAC).**

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

O visor exibirá: -57.473,68 (total de juros pagos entre a 16ª e 27ª parcela).

Pressione a tecla: `[x><y]`

O visor exibirá: -82.105,26 (total de capital amortizado nesse período).

Pressione a tecla: `[+]`

O visor exibirá: -139.578,95 (total pago em parcelas da 16ª à 27ª).

## Títulos de dívida

**Problema: Qual seria o preço justo a ser pago em 28 de abril de 2025 por um título público do Tesouro Nacional, que possui uma taxa nominal de juros de 6,75% ao ano e vence em 14 de junho de 2038, caso você deseje obter uma taxa efetiva de retorno (YTM)[^9] de 4,75% ao ano? Além disso, calcule a taxa efetiva de retorno correspondente ao preço de mercado do título, dado como 122,125%. Considere que o formato de data é dia-mês-ano.**

Pressione as teclas:
```
          [g] [D.MY]
4,75      [i]
6,75      [PMT]
28,042025 [ENTER]
14,062038 [f] [PRICE]
```

O visor exibirá: 119,36% (valor atual do título de dívida, como uma percentagem do valor nominal).

Pressione a tecla: `[+]`

O visor exibirá: 121,87% (valor total, incluindo juros acumulados).

Então, o preço justo a ser pago em 28/04/2025 para obter YTM de 4,75% ao ano é 121,87% do valor nominal.

Calculando agora  a taxa efetiva de retorno considerando que o preço de mercado para o título de dívida é de 122,125%. Pressione as teclas:
```
          [g] [D.MY]
122,125   [PV]
6,75      [PMT]
28,042025 [ENTER]
14,062038 [f] [YTM]
```

O visor exibirá: 4,50% (A taxa efetiva do título de dívida ou *Yield To Maturity*).

## Problemas diversos

**Problema: As vendas de uma empresa foram de R$ 100 milhões no ano inicial. Considerando um crescimento anual composto (CAGR[^10]) de 8% ao ano, qual será o valor das vendas ao final de 10 anos, em milhões de reais?**

Dados do problema:
- n = 10
- i = 8
- PV = -100
- PMT = 0
- FV = ?

Pressione as teclas:
```
10        [n]
8         [i]
100 [CHS] [PV]
          [FV]
```

Resposta: FV = 215,89

**Problema: Sua filha irá para a universidade dentro de 12 anos e você inicia uma poupança com essa finalidade. Ela precisará de R$ 5.000,00 no início de cada mês, durante cinco anos. A poupança rende juros de 1% ao mês, e você planeja efetuar depósitos mensais, começando no final do mês. Quanto você deverá depositar cada mês para poder custear as despesas com a universidade de sua filha no futuro?**

**Etapa 1:** Encontrar o valor presente no momento do último depósito para realizar as retiradas durante o período da faculdade (com pagamentos no início do período).

Dados do problema:
- n = 5 x 12
- i = 1
- PV = ?
- PMT = 5.000
- FV = 0

Pressione as teclas:
```
     [g] [BEG]    (pagamentos feitos no início dos períodos)
5    [g] [12x]
1    [i]
5000 [PMT]
     [PV]
```

O visor exibirá: -227.022,94

**Etapa 2:** Encontrar o valor final após os depósitos de investimento (com depósitos no final do período).

Dados do problema:
- n = 12 x 12
- i = 1
- PV = 0
- PMT = ?
- FV = 227.022,94

Pressione as teclas:
```
         [g] [END]    (pagamentos no final dos períodos)
   [CHS] [STO] [FV]
0        [PV]
12       [g] [12x]
         [PMT]
```

Resposta: R$ 711,53 (depositar cada mês para poder custear as despesas com a universidade da filha)

## Utilização da pilha como constante

**Problema: Para os próximos dez anos, as vendas anuais de uma pequena firma de material eletrônico têm a perspectiva de serem dobradas uma vez por ano. Sendo as vendas atuais de R$ 84.000, quais serão as vendas em cada um dos próximos dez anos?**

Pressione as teclas:
```
2     [ENTER] [ENTER] [ENTER]    (preenche toda a pilha com o valor 2)
84000 [x]
```

O visor exibirá: 168.000,00 (venda do primeiro ano)

Para exibir a venda dos próximos anos, basta pressionar repetidamente a tecla: `[x]`

**Problema: Um trabalhador autônomo pretende economizar R$ 1.213,50 por ano. Se ele mantiver essa meta, quanto ele terá acumulado ao final de cada um dos próximos cinco anos, começando com uma economia inicial de R$ 1.213,50?**

Pressione as teclas:

```
1213,50 [ENTER] [ENTER] [ENTER]    (preenche toda a pilha com o valor 1.213,50)
```

Para exibir os valores acumulados dos anos seguintes, basta pressionar repetidamente a tecla: `[+]`

[^1]: **Anuidade**. Uma anuidade é um tipo de investimento ou empréstimo em que pagamentos iguais são feitos em intervalos regulares, como todo mês ou todo ano. Esses pagamentos podem ocorrer no início ou no final de cada período, dependendo do tipo de anuidade. Por exemplo, se você fizer um pagamento mensal durante um certo tempo, isso caracteriza uma anuidade. Esse conceito é muito usado para calcular valores de empréstimos, financiamentos e investimentos que envolvem pagamentos periódicos. Existem dois tipos principais de anuidade: a ordinária, em que os pagamentos são feitos no final de cada período, e a antecipada, em que os pagamentos são feitos no início dos períodos.

[^2]: **Taxa nominal e taxa efetiva.** A taxa nominal é a taxa de juros divulgada numa base anual, mas que considera capitalização periódica (como mensal ou trimestral). Já a taxa efetiva representa o juro real acumulado, levando em conta a frequência com que os juros são capitalizados durante o ano. Por exemplo, uma taxa nominal de 12% ao ano com capitalização mensal significa que os juros são aplicados mensalmente. Existem esses dois tipos porque a taxa nominal facilita a divulgação e a comparação de ofertas financeiras, simplificando contratos que têm capitalização em períodos menores.

[^3]: **Payback simples**. O *payback* simples é uma forma fácil de calcular quanto tempo leva para um investimento recuperar o dinheiro que foi gasto nele. Basicamente, ele mostra em quantos meses ou anos o valor investido volta, considerando apenas os ganhos ou economias gerados pelo projeto, sem descontar juros ou inflação. Além do *payback* simples, existe também o *payback* descontado, que leva em conta o valor do dinheiro no tempo, ou seja, considera os juros para fazer uma análise mais precisa do retorno do investimento.

[^4]: **Série Uniforme Líquida.** A Série Uniforme Líquida (*Net Uniform Series*), ou Valor Uniforme Líquido, representa uma sequência de pagamentos ou recebimentos iguais que ocorrem em intervalos regulares ao longo do tempo, considerada em termos líquidos.

[^5]: **Desvio padrão.** O desvio padrão mede o quanto os dados variam em relação à média. O *desvio padrão da população* é usado quando temos todos os dados disponíveis e mostra a variação real. Já o *desvio padrão da amostra* é usado quando temos apenas uma parte dos dados (uma amostra) e serve para estimar a variação da população inteira, sendo um pouco maior para compensar a incerteza. Em finanças, geralmente usamos o desvio da amostra, pois raramente temos todos os dados possíveis.

[^6]: **Coeficiente de correlação.** Para saber se a estimativa feita pela regressão linear é confiável, é importante observar o coeficiente de correlação de Pearson. Esse número mostra o quanto os dados seguem uma linha reta. Se ele estiver próximo de 1 ou de -1, significa que os pontos estão bem alinhados e a previsão tende a ser precisa. Mas se estiver próximo de 0, os dados estão espalhados e o modelo não é muito confiável para fazer previsões.

[^7]: **Taxa contínua.** A taxa contínua é uma taxa de juros usada em contextos financeiros e matemáticos onde a capitalização ocorre de forma ininterrupta, ou seja, os juros são aplicados continuamente ao saldo. Diferente das taxas com capitalização em períodos discretos (como mensal ou anual), a taxa contínua usa uma fórmula baseada em exponenciais, onde *e* é a base dos logaritmos naturais. Esse tipo de taxa é comum em modelos financeiros mais avançados, como no cálculo de crescimento exponencial ou precificação de ativos.

[^8]: **Hipoteca e Alienação Fiduciária.** A hipoteca e a alienação fiduciária são formas de garantia usadas em financiamentos. Na hipoteca, o bem fica no nome do devedor, e o credor precisa entrar com ação judicial se o pagamento não for feito. Já na alienação fiduciária, o bem é transferido ao credor em caráter provisório até a quitação da dívida, o que facilita a retomada do bem em caso de inadimplência, sem necessidade de processo judicial. No Brasil, a alienação fiduciária é a forma mais usada por ser mais rápida e segura para os credores.

[^9]: **Yield To Maturity.** A *Yield To Maturity* (YTM) representa a taxa efetiva do título de dívida. Ela reflete o rendimento (*yield*) do título de renda fixa até seu vencimento (*maturity*).

[^10]: **Taxa de Crescimento Anual Composta.** A CAGR (*Compound Annual Growth Rate*), é uma medida que mostra a taxa média de crescimento de um investimento ou negócio durante um período específico, considerando o efeito dos juros compostos. Ele indica quanto algo cresceu, em média, por ano, partindo do valor inicial até o valor final, mesmo que o crescimento tenha variado a cada ano. Isso ajuda a entender o desempenho real ao longo do tempo.

[^11]: **Leasing.** O arrendamento mercantil, *leasing*, é uma modalidade de financiamento onde uma empresa (a financeira) compra um bem (por exemplo, um carro) e o cede ao usuário (arrendatário) para uso, mediante pagamentos periódicos. Funciona como um aluguel com opção de compra no final do contrato. Durante o contrato, o usuário paga uma espécie de "aluguel" (as parcelas do *leasing*) e, ao final do período, pode optar por comprar o bem pagando um valor residual acordado.
