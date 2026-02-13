# 📈 Portfolio Optimization with Time Series Forecasting

> Predicting market trends to optimize investment portfolios using advanced forecasting models

**Built for GMF Investments** — Where data science meets portfolio management.

---

## 🎯 What This Project Does

This project helps financial advisors and investors make data-driven portfolio decisions by:

1. **Analyzing** historical data for TSLA, BND, and SPY (2015–2026)
2. **Forecasting** Tesla (TSLA) prices with SARIMA (and optionally LSTM)
3. **Optimizing** asset allocation using Modern Portfolio Theory (MPT)
4. **Backtesting** the strategy against a 60/40 SPY/BND benchmark
5. **Reporting** findings in a professional investment memo (PDF-ready)

Think of it as a data-driven approach to investments—grounded in statistical analysis and risk metrics rather than guesswork.

---

## 📊 Assets We Analyze

| Asset | Ticker | Description |
|-------|--------|-------------|
| **Tesla** | TSLA | High-growth, high-volatility stock |
| **Vanguard Total Bond Market ETF** | BND | Low-risk stability anchor |
| **S&P 500 ETF** | SPY | Diversified market exposure |

Together they provide growth potential, stability, and diversification.

---

## 📁 Project Structure

```
portfolio-optimization-forecasting/
├── notebooks/
│   ├── task1_preprocessing_eda.ipynb    # Data extraction, cleaning, EDA, risk metrics
│   ├── task2_forecasting_models.ipynb   # SARIMA (and LSTM) forecasting, model comparison
│   ├── task3_forecast_future_trends.ipynb  # 12-month forecasts, confidence intervals
│   ├── task4_portfolio_optimization.ipynb  # MPT, Efficient Frontier, portfolio recommendation
│   ├── task5_backtesting_strategy.ipynb   # Strategy vs benchmark backtest
├── data/
│   └── processed/                      # Processed CSVs and generated figures
├── scripts/
├── src/
├── tests/
├── requirements.txt
└── README.md
```

---

## 🚀 Quick Start

### 1. Install dependencies

```bash
pip install -r requirements.txt
```

### 2. Run notebooks in order

Run the notebooks **in sequence** (Task 1 → 2 → 3 → 4 → 5). Later tasks depend on outputs from earlier ones.

| Order | Notebook | Purpose |
|-------|----------|---------|
| 1 | `task1_preprocessing_eda.ipynb` | Load YFinance data, clean, EDA, stationarity tests, VaR, Sharpe |
| 2 | `task2_forecasting_models.ipynb` | Train SARIMA (LSTM optional), compare models, save forecasts |
| 3 | `task3_forecast_future_trends.ipynb` | Generate 12-month TSLA forecast with confidence intervals |
| 4 | `task4_portfolio_optimization.ipynb` | Build Efficient Frontier, Max Sharpe & Min Vol portfolios |
| 5 | `task5_backtesting_strategy.ipynb` | Backtest strategy vs 60/40 SPY/BND benchmark |

### 3. Generate the final report (PDF)

- **Jupyter:** Open `final_report.ipynb` → run all cells → **File → Download as → PDF via LaTeX** (or print to PDF).
- **Command line:** `jupyter nbconvert --to pdf notebooks/final_report.ipynb` (requires `nbconvert` and LaTeX for PDF).

---

## 🛠️ Technologies & Methods

- **Data:** yfinance, pandas  
- **Time series:** statsmodels (ARIMA/SARIMA), pmdarima (auto_arima)  
- **Optional ML:** TensorFlow/Keras (LSTM) — can be skipped if not installed  
- **Portfolio:** PyPortfolioOpt (Efficient Frontier)  
- **Metrics:** VaR, Sharpe ratio, MAE, RMSE, MAPE, max drawdown  

---

## 💡 Notes

- **LSTM:** Task 2 can run with SARIMA only; LSTM is optional and may be skipped if TensorFlow is not available. The comparison table uses SARIMA as the selected model in that case.


---

*Built for GMF Investments — Time Series Forecasting for Portfolio Management Optimization*
