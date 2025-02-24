# Macroeconometrics

![Gere uma imagem sobre macroeconometria 20-02-2025 at 06-30-35](https://github.com/user-attachments/assets/99ef8ada-2357-47c9-a2c3-0cf2e57d471a)


> A macroeconomia é um ramo da ciência econômica que estuda o comportamento de uma economia como um todo. Dessa forma, os macroeconomistas buscam entender os fenômenos econômicos formulando modelos agredados (representações simplificadas da realidade), eles são agregados, porque parte-se do pressuposto de que o todo é mais complexo do que a soma das partes, não sendo possível descrever uma economia por meio de modelos para todas as empresas e indivíduos. Sendo assim, sua preocupação está em analisar indicadores agregados como PIB, taxa de desemprego e índices de preços.

### Conceitos fundamentais

- Ceteris paribus: "todo o mais é constante", ou seja, nada muda, exceto o fator ou fatores que estão sendo estudados
- Variável endógena: também chamada de dependente, é a variável cujos valores são determinados no modelo
- Variável exógena: também chamada de independente, é a variável cujos valores são determinados fora do modelo
- Preços flexíveis: Suposição de que os preços se ajustam para igualar oferta e demanda (longo prazo)
- Preços rígidos: Suposição de que no curto prazo, muitos preços são rígidos, ou seja, se ajustam lentamente em resposta a mudanças na oferta ou na demanda
- Fluxo: Magnitude econômica de um intervalo de tempo. EX: PIB (taxa mensal)
- Estoque: Magnitude medida de um determinado ponto específico no tempo. EX: dívida externa do país

> Quando estamos trabalhando com valores macroeconômicos é normal que eles sofram variações ao longo do tempo. Sendo assim, para termos uma visão realística dos dados, sempre transformamos valores nominais para valores deflacionados (ou reais), ou seja, contabilizando o efeito da variações dos indicadores economicos, geralmente o efeito inflacionário do período. Então para exemplificar, vamos pegar uma série do salário mínimo (IPEADATA) é um índice de preços (Índice Nacional de Preços ao Consumidor Amplo - IPCA), que será nossa variável para deflacionar o salário mínimo, aplicando à fórmula:

$Vreal(x,y) = (\frac{Ix}{Iy}) * Vx$

onde: 
- $Vreal(x,y)$ = é o valor real, ou deflacionado, no período x na data-base y
- $Ix$ = é o índice de preços fixado na data-base y
- $Iy$ = é o índice de preços no período x
- $Vx$ =  é o valor ou preço nominal no período x

Exemplo: Imagine que queremos o salário mínimo real de julho de 2021 (07/2021) na data-base de dezembro de 2021 (12/2021)

|Data |Salário Minimo|IPCA|
|---	     |--- |---    |
|2021-12-01|1100|6330.59|   
|2021-11-01|1100|6284.71|   
|2021-10-01|1100|6232.36|   	
|2021-09-01|1100|6160.89|  
|2021-08-01|1100|6087.84|  
|2021-07-01|1100|6034.73|  

$Vreal(x,y) = (\frac{Ix}{Iy}) * Vx$

$Vreal$(07/21,12/21) = $(\frac{6330.59}{6034.73}) * 1100$






































































### The Brazilian Central Bank Models

1. Small-scale semi-structural models
2. Vector Autoregressive (VAR) Models
3. Leading and core inflation indicators
6. Medium semi-structural model (PAGODE)
7. Medium-sized Micro-Founded Model (SAMBA)

### Small-Scale Semi-Structural Models

> In 1990, macroeconomic theory began to be based on the neoclassical synthesis or new macroeconomic consensus. The implications of this were the development of small structural models, which made it possible to estimate the lags in the effect of changes in the monetary policy instrument on prices.

Model Assumptions: 
- Inflation depends on the real interest rate
- Nominal base interest rate is the instrument of monetary policy
- Agents' expectations can be backward-looking (past information) or forward-looking (future expectations)
- There are transmission mechanisms in monetary policy decisions and they have transmission lags

> The new consensus or new Keynesianism admits short-term subequilibria, derived from market failures, that is, the output gap may be non-zero in the short term. Therefore, the BC's small-scale models seek to capture the transmission mechanisms of monetary policy decisions, as well as the lags involved, and are composed of:

- IS Curve (Demand)
- Phillips Curve (Supply)
- Interest Rate Parity (Contact with the external sector)
- Taylor Rule (Monetary Policy Decisions)

> Interest Rate Parity or Uncovered Interest Rate Parity Condition is a concept that describes the relationship between the interest rates of two countries and the expected exchange rates between their currencies. This condition is important for understanding how interest rates and exchange rate expectations influence capital flows between countries.

#### Mathematically:
IS Curve -> $Ht = \beta0 - \beta1(it - Etπt+1 - r*) + β2Θt−1 + β3Ψt−1 + εt$

- Ht = Product gap
- it = Nominal interest rate
- Etπt+1 = Expectation at t for inflation at t + 1
- r∗ = Neutral interest rate
- Θt−1 = Real exchange rate
- Ψt−1 = Public sector financing needs
- εt = Demand shock

Phillips Curve -> $πt = α0 + α1πt−1 + α2Etπt+1 + α3ht−1 + α4∆εt + εt$

- πt = Inflation
- ∆εt = First difference of nominal exchange rate
- εt = Supply shock

Interest Rate Parity -> $∆εt = φ0 φ1(it − it*) + φ2xt + εt$

- (it − it*) = Interest differential
- xt = Risk premium
- εt = External shock

Taylor Rule -> $it = ω0 + ω1it−1 + ω2(Etπt+1 − π∗) + ω3ht + ω4∆εt + εt$

- π∗ = Inflation target
- εt = white noise

### Bibliographical References:
- W.H. Greene. Econometric Analysis. Pearson Education, 2003.
- C. A. Sims. Macroeconometrics and reality. Econometrica,
- E. J. A. Lima, F. Araujo, and J. R. Costa e Silva. Previsáo e Modelos Macroeconômicos no Banco Central do Brasil. Dez anos de metas para inflação no Brasil, 2010.
- J. M. Wooldridge. Introductory Econometrics: A Modern Approach. Editora Cengage, 2013
