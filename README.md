# Case Momentum — Trainee Quant

Backtest de uma carteira long-only de momentum 12-1 (top 5 de um universo de 20 ações da B3, pesos iguais,
rebalanceamento mensal), comparada com o Ibovespa de 2016 a 2025.

## Como rodar

```bash
python -m venv .venv
.venv\Scripts\activate        # Windows (Linux/macOS: source .venv/bin/activate)
pip install -r requirements.txt
jupyter nbconvert --to notebook --execute momentum_case.ipynb --output momentum_case.ipynb
```

Os preços e o CDI ficam em cache em `data/`. Para baixar tudo de novo, use `FORCE_DOWNLOAD = True` na célula de configuração.

## Conteúdo

- `momentum_case.ipynb` — notebook com dados, sinal, verificação de look-ahead, métricas, gráficos, respostas e limitações
- `enunciado/` — enunciado original (.docx) e versão em texto (.md)
- `requirements.txt` — dependências
- `data/` — cache dos preços (yfinance) e do CDI (BCB/SGS 4391)
- `figures/` — gráficos exportados (PNG)
