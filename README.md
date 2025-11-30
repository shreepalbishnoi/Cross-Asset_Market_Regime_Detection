# HMM-Market_Regime_Detector
Applying unsupervised learning (HMM) to financial time-series to uncover hidden market states. This project develops and evaluates a regime-based trading strategy against the S&amp;P 500 benchmark.
Of course. Let's level up your GitHub project to make it stand out for quant roles.

[![Python Version](https://img.shields.io/badge/Python-3.9%2B-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Status](https://img.shields.io/badge/status-complete-brightgreen.svg)]()

### A Quantitative Approach to Dynamic Asset Allocation using Hidden Markov Models

This project demonstrates a quantitative framework for identifying hidden market regimes from cross-asset financial data. It leverages a **Hidden Markov Model (HMM)** to uncover underlying market states (e.g., Bull, Bear, Volatile) and deploys a **Tactical Asset Allocation (TAA)** strategy based on these regimes. The strategy's performance is rigorously backtested against the S&P 500 benchmark to evaluate its effectiveness and potential to generate alpha.

The core thesis is that by dynamically shifting allocations based on the prevailing economic regime, a portfolio can enhance risk-adjusted returns and reduce major drawdowns compared to a static buy-and-hold strategy.

---

### ## Key Visualization: Market Regimes on the S&P 500

The plot below shows the model's output, shading the S&P 500 price history according to the predicted market regime. This visual validation is the centerpiece of the analysis.
<img width="4465" height="2362" alt="market_regimes" src="https://github.com/user-attachments/assets/addb0157-b491-4f0c-8d77-fe49aad79df3" />
<img width="1489" height="790" alt="backtest_performance" src="https://github.com/user-attachments/assets/60099afa-c27c-4d7d-addd-a4a4dd7eb770" />


---

### ## Core Features

- **Multi-Source Data Integration**: Fetches data from `yfinance` (market) and `FRED` (economic) APIs.
- **Unsupervised Regime Detection**: Employs a `GaussianHMM` to identify 4 distinct market regimes from features like equity returns, volatility (VIX), and credit spreads.
- **Dynamic Backtesting Engine**: Implements and evaluates a TAA strategy against a 100% S&P 500 benchmark.
- **Performance Analytics**: Calculates key metrics including **CAGR, Annualized Volatility, Sharpe Ratio, Maximum Drawdown, and Alpha**.

---

### ## Tech Stack & Libraries

- **Language**: **Python 3.9+**
- **Core Libraries**:
  - `pandas` for data manipulation
  - `numpy` for numerical operations
  - `scikit-learn` for data scaling
  - `hmmlearn` for the Hidden Markov Model
  - `yfinance` & `fredapi` for data acquisition
  - `matplotlib` & `seaborn` for visualization

---


---

### ## Setup and Usage

**1. Clone the Repository**
```bash
git clone [https://github.com/YourUsername/HMM-Market-Regime-Detector.git](https://github.com/YourUsername/HMM-Market-Regime-Detector.git)
cd HMM-Market-Regime-Detector
````

**2. Create and Activate a Virtual Environment**

```bash
# For Unix/macOS
python3 -m venv venv
source venv/bin/activate

# For Windows
python -m venv venv
venv\Scripts\activate
```

**3. Install Dependencies**

```bash
pip install -r requirements.txt
```

**4. Add Your FRED API Key**
This project requires a free API key from the Federal Reserve Economic Data (FRED).

1.  Obtain your key from the [FRED website](https://fred.stlouisfed.org/docs/api/api_key.html).
2.  Open the script/notebook and set the `FRED_API_KEY` variable:
    ```python
    FRED_API_KEY = 'YOUR_API_KEY_HERE'
    ```

**5. Run the Analysis**
You can run either the Python script or walk through the Jupyter Notebook.

```bash
jupyter notebook fin_proj.ipynb
```

The script will execute the full pipeline and generate the plots showcasing the regimes and backtest results.

