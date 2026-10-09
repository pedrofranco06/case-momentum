# Case Trainee Quant — Estratégia de Momentum

(Versão em texto do arquivo `Case_Momentum_Trainee_Quant.docx`, para leitura fácil.)

## O método

Ações que mais subiram nos últimos meses tendem a continuar performando melhor. Usaremos o **momentum 12-1**: retorno acumulado dos últimos 12 meses, descartando o mês mais recente para evitar o efeito de reversão de curto prazo.

    MOM(i,t) = P(i,t−1) / P(i,t−12) − 1

## Enunciado

Monte uma carteira long-only que, todo mês, compra as 5 ações com maior momentum 12-1 de um universo fixo de 20 ações da B3, e compare com o Ibovespa.

| Parâmetro  | Valor |
|------------|-------|
| Universo   | PETR4, VALE3, ITUB4, BBDC4, BBAS3, ABEV3, WEGE3, B3SA3, RENT3, SUZB3, GGBR4, EMBR3, EQTL3, RADL3, LREN3, PRIO3, VIVT3, CMIG4, SBSP3, TOTS3 |
| Dados      | yfinance, preços ajustados, 2016 a 2025, frequência mensal |
| Carteira   | Top 5 do ranking, pesos iguais, rebalanceamento mensal, sem custos |
| Benchmark  | Ibovespa (^BVSP) |

## Tarefas

1. Baixar os dados, mensalizar e calcular o sinal 12-1, sem look-ahead (explicar como foi garantido).
2. Montar a carteira e calcular retorno anualizado, volatilidade, Sharpe e máximo drawdown, para ela e para o Ibovespa.
3. Plotar a curva de capital acumulado (base 100) contra o Ibovespa.

## Perguntas

1. A estratégia bateu o Ibovespa ajustado ao risco? Em que períodos falhou?
2. Que viés o universo escolhido hoje introduz no resultado?
3. Por que pular o último mês na formação do sinal?

## Entrega

Notebook .ipynb que rode do início ao fim, com as métricas, o gráfico e as respostas às perguntas.
