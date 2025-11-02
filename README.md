![EMA Crossover Visualization](/img/image-2.png)

# 📊 Exponential Moving Average (EMA) Crossover Trading Strategy

### 🧭 Trend-Following Strategy with Automated Parameter Optimization (Python)

---

This project presents a **multi-asset Exponential Moving Average (EMA) Crossover Trading Strategy** implemented in Python.  
The system detects **momentum shifts** by comparing short-term and long-term EMAs and generates **Buy** and **Sell** signals automatically.

The analysis combines **technical theory** with **quantitative backtesting**, producing interpretable trading insights and clear visualizations.

---

## 📊 Data & Assets

The strategy analyzes daily price data for **10 major UK-listed companies** across various sectors.  
All data were obtained using [`yfinance`](https://pypi.org/project/yfinance/).

| Ticker | Company Name | Sector |
|---------|---------------|--------|
| **AZN.L** | AstraZeneca plc | Healthcare / Pharmaceuticals |
| **HSBA.L** | HSBC Holdings plc | Financials / Banking |
| **SHEL.L** | Shell plc | Energy / Oil & Gas |
| **ULVR.L** | Unilever plc | Consumer Goods / Household Products |
| **BP.L** | BP plc | Energy / Oil & Gas |
| **DGE.L** | Diageo plc | Consumer Goods / Beverages |
| **GSK.L** | GSK plc | Healthcare / Pharmaceuticals |
| **BATS.L** | British American Tobacco plc | Consumer Goods / Tobacco |
| **RIO.L** | Rio Tinto plc | Basic Materials / Mining |
| **REL.L** | Relx plc | Technology / Information & Analytics |

These assets were selected to represent **diversified exposure** across major LSE sectors — including Energy, Healthcare, Financials, and Consumer Goods — ensuring the strategy was tested on **different volatility and trend profiles**.

---

## ⚙️ Key Features

✅ Downloads real stock data via [`yfinance`](https://pypi.org/project/yfinance/)  
✅ Computes short-term and long-term EMAs with adjustable windows  
✅ Generates crossover-based **Buy/Sell** signals  
✅ Performs **grid search optimization** for the best EMA combinations  
✅ Evaluates performance using **Sharpe Ratio**, **Total Return**, and **Max Drawdown**  
✅ Produces detailed visual backtests for each ticker  

---

## 🧮 Methodology

### 1️⃣ EMA Calculation
The **Exponential Moving Average (EMA)** applies exponentially decreasing weights to older prices, allowing faster adaptation to recent market movements compared to the Simple Moving Average (SMA).

\[
EMA_t = \alpha P_t + (1 - \alpha) EMA_{t-1}, \quad \alpha = \frac{2}{N+1}
\]

- **Short EMA** → Captures short-term price momentum.  
- **Long EMA** → Represents the broader trend.

### 2️⃣ Signal Generation
Trading signals are created based on EMA crossovers:

- **Buy Signal:** Short EMA crosses **above** Long EMA → Uptrend confirmation  
- **Sell Signal:** Short EMA crosses **below** Long EMA → Downtrend confirmation  

### 3️⃣ Backtesting Metrics
Each EMA pair is backtested using three key metrics:

| Metric | Description |
|---------|--------------|
| **Total Return** | Compound portfolio growth over the test period |
| **Sharpe Ratio** | Average excess return per unit of volatility |
| **Max Drawdown** | Maximum observed portfolio loss from peak to trough |

---

## 📈 Sample Visualization

Below is an example of EMA crossover signals plotted over historical prices.  
Green ▲ markers indicate Buy signals, while red ▼ markers indicate Sell signals.

![EMA Crossover Signals Example](/img/image-2.png)

---

