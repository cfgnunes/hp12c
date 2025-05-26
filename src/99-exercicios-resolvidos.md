# Exercícios resolvidos com a HP 12c

## Pagamentos únicos

**As vendas de uma empresa foram de R$ 100 milhões. Se as vendas crescerem 8% ao ano, qual será o valor em 10 anos, em milhões?**

```
n = 10
i = 8
PV = -100
PMT = 0
FV = ?
```

Resposta: FV = 215,89

**Suponha que um título do governo pagará R$ 1.000,00 daqui a três anos. Se a taxa de juros dos títulos de 3 anos é de 4% ao ano, quanto vale esse título hoje?**

```
n = 3
i = 4
PV = ?
PMT = 0
FV = 1.000
```

Resposta: PV = -889,00

**O Tesouro Nacional oferece um título por R$ 613,81. Nenhum pagamento será feito até o vencimento, em 10 anos, quando será resgatado por R$ 1.000,00. Qual a taxa de juros efetiva anual desse título?**

```
n = 10
i = ?
PV = -613,81
PMT = 0
FV = 1.000
```

Resposta: i = 5

## Pagamentos únicos - Investimentos

**Você investe R$ 5.000,00 em uma conta que rende 6% ao ano durante 8 anos. Qual será o valor ao final do período?**

```
n = 8
i = 6
PV = -5.000
PMT = 0
FV = ?
```

Resposta: FV = 7.969,24

**Você precisa de R$ 10.000,00 em 5 anos. A conta rende 7% ao ano. Quanto deve investir agora?**

```
n = 5
i = 7
PV = ?
PMT = 0
FV = 10.000
```

Resposta: PV = -7.129,86

**Você investe R$ 2.000,00 e o valor cresce para R$ 2.800 em 4 anos. Qual foi a taxa de juros anual?**

```
n = 4
i = ?
PV = 2.000
PMT = 0
FV = 2.800
```

Resposta: i = 8,78

**Você investe R$ 3.000,00 e o valor dobra para R$ 6.000,00 com juros de 9% ao ano. Quanto tempo levou?**

```
n = ?
i = 9
PV = -3.000
PMT = 0
FV = 6.000
```

Resposta: n = 8,04 (anos)

Nota: A calculadora HP 12c retorna o valor 9, em vez de 8,04, porque arredonda automaticamente o resultado para cima em cálculos que envolvem a determinação do número de períodos (n). Ela obtém apenas valores inteiros para n, sendo uma limitação da calculadora.

**Você aplica R$ 1.000,00 por 10 anos em um banco que paga 5% ao ano, com pagamento no final do período. Quanto terá ao final?**

```
n = 10
i = 5
PV = -1.000
PMT = 0
FV = ?
```

Resposta: FV = 1.628,89

**O Sr. Carlos pretende investir R$ 10.000,00 em uma aplicação com juros compostos de 8% ao ano, capitalizados trimestralmente. Qual será o valor futuro após 5 anos?**

```
n = 5 x 4
i = 8 / 4
PV = -10.000
PMT = 0
FV = ?
```

Resposta: FV = 14.859,47

**Quanto é preciso depositar hoje para ter R$ 8.000,00 em 5 anos, com juros de 6,5% ao ano capitalizados mensalmente?**

```
n = 5 x 12
i = 6,5 / 12
PV = ?
PMT = 0
FV = 8.000
```

Resposta: PV = -5.785,29

**O Sr. Roberto vai se aposentar em 20 anos e quer comprar uma casa de R$ 2.000.000,00. Quanto ele precisa investir hoje em um banco que paga 9% ao ano com capitalização semestral?**

```
n = 20 x 2
i = 9 / 2
PV = ?
PMT = 0
FV = 2.000.000
```

Resposta: PV = -343.857,40

## Pagamentos únicos - Empréstimos

**Você toma emprestado R$ 7.000,00 a uma taxa de 5% ao ano por 3 anos. Qual será o valor total a ser pago?**

```
n = 3
i = 5
PV = -7.000
PMT = 0
FV = ?
```

Resposta: FV = 8.103,38

**Você deve pagar R$ 10.000,00 em 6 anos. A taxa anual juros é de 4%. Quanto pode pegar emprestado hoje?**

```
n = 6
i = 4
PV = ?
PMT = 0
FV = -10.000
```

Resposta: PV = 7.903,15

**Você tomou R$ 1.500,00 emprestados e pagou R$ 1.800,00 após 2 anos. Qual foi a taxa de juros?**

```
n = 2
i = ?
PV = 1.500
PMT = 0
FV = -1.800
```

Resposta: i = 9,54

**Você tomou R$ 5.000,00 emprestados e pagou R$ 6.000,00 com juros anuais de 8%. Quanto tempo demorou?**

```
n = ?
i = 8
PV = 5.000
PMT = 0
FV = 6.000
```

Resposta: n = 2,37 (anos)

Nota: A calculadora HP 12c retorna o valor 3, em vez de 2,37, porque arredonda automaticamente o resultado para cima em cálculos que envolvem a determinação do número de períodos (n). Ela obtém apenas valores inteiros para n, sendo uma limitação da calculadora.

**Se João empresta R$ 1.500,00 a um amigo com taxa de 4,3% ao ano, capitalizada mensalmente, quanto de juros terá ao final de um ano?**

```
n = 1 x 12
i = 4,3 / 12
PV = -1.500
PMT = 0
FV = ?
```

Resposta: FV = 1.565,79 | Juros = 65,79

**Lucas pegou R$ 600,00 emprestados no banco e esse valor quadruplicou em 2 anos, com capitalização mensal. Qual foi a taxa de juros?**

```
n = 2 x 12
i = ?
PV = -600
PMT = 0
FV = 2.400
```

Resposta: i = 5,9463 x 12 = 71,36%

## Investimentos com depósitos periódicos

**André deposita R$ 22.000,00 ao final de cada ano por 7 anos, em uma conta que rende 6% ao ano. Quanto ele terá ao final do período?**

```
n = 7
i = 6
PV = 0
PMT = -22.000
FV = ?
```

Resposta: FV = 184.664,43

**Marcela deposita R$ 1.200,00 no final de cada trimestre por 10 anos, em uma conta que rende 8% ao ano com capitalização trimestral. Quanto terá ao final do período?**

```
n = 10 x 4
i = 8 / 4
PV = 0
PMT = -1.200
FV = ?
```

Resposta: FV = 72.482,38

**Carlos quer se aposentar em 20 anos e, para isso, deposita R$ 200,00 no final de cada mês em um fundo que rende 7,2% ao ano com capitalização mensal. Quanto terá ao se aposentar?**

```
n = 20 x 12
i = 7,2 / 12
PV = 0
PMT = -200
FV = ?
```

Resposta: FV = 106.752,47

**Juliana quer se aposentar em 32 anos e planeja investir mensalmente em uma conta que rende 9% ao ano. Quanto precisa investir por mês para acumular R$ 2.000.000,00?**

```
n = 32 x 12
i = 9 / 12
PV = 0
PMT = ?
FV = 2.000.000
```

Resposta: PMT = -902,32

## Anuidade ordinária (pagamentos no final do período)

**Você pode comprar uma anuidade que paga R$ 1.000,00 no final de cada ano por 5 anos. Se você pode ganhar 6% ao ano em outros investimentos de mesmo risco, qual o valor máximo que deve pagar?**

```
n = 5
i = 6
PV = ?
PMT = 1.000
FV = 0
```

Resposta: PV = -4.212,36

**Você herdou R$ 200.000,00 e investe a 6% ao ano. Quanto pode sacar no final de cada um dos próximos 15 anos?**

```
n = 15
i = 6
PV = 200.000
PMT = ?
FV = 0
```

Resposta: PMT = -20.592,55

## Anuidade antecipada (pagamentos no início do período)

**Com uma taxa de juros de 0,75% ao mês, quanto deve ser depositado mensalmente (no início do mês) para atingir R$ 100.000,00 em 5 anos?**

```
n = 5 x 12
i = 0,75
PV = 0
PMT = ?
FV = 100.000
```

Resposta: PMT = -1.315,97

**Com uma taxa de juros de 1% ao mês, quanto deve ser depositado mensalmente (no início do mês) para acumular R$ 1.000.000,00 em 20 anos?**

```
n = 20 x 12
i = 1
PV = 0
PMT = ?
FV = 1.000.000
```

Resposta: PMT = -1.000,85

**Ricardo deposita R$ 500,00 no início de cada trimestre durante 7 anos, em uma conta com juros de 12% ao ano, capitalizados trimestralmente. Quanto ele terá ao final do período?**

```
n = 7 x 4
i = 12 / 4
PV = 0
PMT = -500
FV = ?
```

Resposta: FV = 22.109,43

## Financiamentos e empréstimos com parcelas fixas (tabela Price)

**Você está comprando sua primeira casa por R$ 220.000,00 e pagará R$ 30.000,00 de entrada. Vai financiar os R$ 190.000,00 restantes em um empréstimo de 30 anos, com taxa nominal de 7% ao ano e parcelas fixas mensais (tabela Price). Qual será o valor das parcelas mensais?**

```
n = 30 x 12
i = 7 / 12
PV = 190.000
PMT = ?
FV = 0
```

Resposta: PMT = -1.264,07

**Você quer comprar um carro de R$ 28.000,00. A concessionária oferece taxa de 4% ao ano para 48 meses. Quais serão as parcelas fixas mensais?**

```
n = 4 x 12
i = 4 / 12
PV = 28.000
PMT = ?
FV = 0
```

Resposta: PMT = -632,21

**Maria possui um empréstimo consignado, com 96 parcelas fixas (tabela Price) de R$ 1.340,00, das quais já pagou 13, restando um saldo devedor de R$ 42.458,51. Determine a taxa de juros anual com capitalização mensal e, em seguida, calcule quantas parcelas seriam eliminadas caso ela amortizasse R$ 1.000,00 hoje, utilizando amortização por tempo. Calcule também o novo valor da parcela caso ela optasse por realizar a amortização por valor da parcela.**

```
n = 83 (96 - 13)
i = ?
PV = 42.458,51
PMT = -1.340,00
FV = 0
```

Resposta: i = 2,85

```
n = ?
i = 2,85
PV = 41.458,51 (retirado R$ 1.000,00 do saldo devedor de R$ 42.458,51)
PMT = -1.340,00
FV = 0
```

Resposta: n = 76. Logo, 83-76 = 7 parcelas eliminadas (amortização por tempo).

```
n = 83 (96 - 13)
i = 2,85
PV = 41.458,51 (retirado R$ 1.000,00 do saldo devedor de R$ 42.458,51)
PMT = ?
FV = 0
```

Resposta: PMT = -1.308,48 (novo valor da parcela após amortização por parcela).

## Financiamentos e empréstimos com parcelas decrescentes (tabela SAC)

Para os exercícios abaixo, utilize o programa para HP 12c [Amortização pelo Sistema de Amortização Constante (Tabela SAC)](./03-tabela-sac.md).

**Considere um empréstimo de R$ 500.000,00, com taxa de juros de 2% ao mês e prazo total de 20 meses. Com base nessas condições, calcule o total de juros pagos até a 13ª parcela, bem como o valor total pago até essa mesma parcela. Considere o Sistema de Amortização Constante (SAC).**

Pressione as teclas:

```
20 n
2 i
500000 PV
13 R/S
```

O visor exibirá: -91.000,00 (total de juros pagos até a 13ª parcela).

Pressione a tecla `+`

O visor exibirá: -416.000,00 (total pago até a 13ª parcela).

**Considere um empréstimo no valor de R$350.000,00, com taxa de juros de 1% ao mês e prazo de 35 meses. Com base nesses dados, determine os juros pagos especificamente na 28ª parcela, bem como o valor total dessa parcela. Considere o Sistema de Amortização Constante (SAC).**

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

O visor exibirá: -800,00 (juros pagos somente na 28ª parcela).

Pressione as teclas:

```
RCL PMT
```

O visor exibirá: -10.800,00 (valor da 28ª parcela).

**Considere um empréstimo no valor de R$ 320.000,00, com taxa de juros de 3% ao mês e prazo total de 42 meses. Com base nessas condições, calcule o total de juros pagos ao longo de todo o financiamento, assim como o valor total desembolsado com o pagamento das parcelas durante todo o período. Considere o Sistema de Amortização Constante (SAC).**

Pressione as teclas:

```
320000 PV
3 i
42 n
42 R/S
```

O visor exibirá: -206.400,00 (total de juros pagos durante todo o financiamento).

Pressione a tecla `+`

O visor exibirá: -526.400,00 (total pago em parcelas ao longo de todo o financiamento).

**Considere um empréstimo no valor de R$260.000,00, com taxa de juros de 4% ao mês e prazo total de 38 meses. Com base nessas condições, calcule, para o período entre a 16ª e a 27ª parcela: o total de juros pagos, o total de amortizações realizadas e o valor total desembolsado com o pagamento dessas parcelas. Considere o Sistema de Amortização Constante (SAC).**

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

O visor exibirá: -57.473,68 (total de juros pagos entre a 16ª e 27ª parcela).

Pressione a tecla `x><y`

O visor exibirá: -82.105,26 (total de capital amortizado nesse período).

Pressione a tecla `+`

O visor exibirá: -139.578,95 (total pago em parcelas da 16ª à 27ª).
