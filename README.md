# USD to INR 100-Year Continuum \& Macro Analysis Terminal

An interactive macroeconomic engine exploring USD/INR exchange rate trajectories (1947–2050). The framework optimizes a 3-regime piecewise global trend break structure and models future horizons using ARIMA upward drift vectors and seasonal Prophet curves.

## Local Installation \& Setup

1. **Clone the Repository**

```
git https://github.com/vinay-y2k/currency-analysis.git
cd currenct-analysis
```

2. **Configure Environment and Dependencies**

```
python -m venv venv
.\\venv\\Scripts\\activate  # Linux:source venv/bin/activate
pip install -r requirements.txt
```

_Note: Resolving the deep learning layer automatically installs the `torch` runtime to process self-attention weights locally on your CPU._

3. **Configure Credentials**
   Create a `.env` file in the root directory:

```
FRED_API_KEY=your_st_louis_fed_api_key
```

4. **Execute Pipeline**

```
python main.py
```

## Interactive Architecture & Modeling Matrix

- **100-Year Interactive Engine:** Fully self-contained Plotly charting system embedded directly in HTML via `include_plotlyjs=True`. Works completely offline without needing an active Python kernel or server runtime.
- **Deterministic Reproducibility:** Anchored using global seed states across Python, NumPy, and PyTorch random number generators to ensure identical Chronos sample outputs across sequential executions.
- **Structural Break Tracking:** Automates mathematical regime break optimizations detailing early currency pegs vs. modern floating policies.
- **Multi-Model Forecast Spectrum:**
  - **ARIMA (1,1,0) with Drift:** Captures the structural upward drift driven by deterministic linear time trend variables.
  - **Prophet:** Maps seasonal macro waves and annual variations using amplified historical volatility scaling.
  - **Amazon Chronos (T5-Small):** Processes the modern float era as an attention context vector to generate a non-linear, self-correcting asset trajectory path.
- **Cross-National Metrics Matrix:** Contextualizes global market data profiles tracking policy mandates, billionaire asset distributions (US: 989, India: 229), and systemic well-being indices (US: 23rd, India: 116th) across the United States and India.

## Data Sources & Citations

This pipeline ingests and standardizes macro-financial timelines from the following primary endpoints:

- **Modern Floating Era (1973–Present):** Automated sequence ingestion from the **Federal Reserve Bank of St. Louis (FRED) API Resource Engine**.
  - _Series ID Identifier:_ `DEXINUS` (Indian Rupees to One U.S. Dollar Spot Exchange Rate).
- **Historical Sovereign Peg Era (1947–1973):** Extrapolated from historic central reserve matrices charting structural currency adjustments:
  - _1947-08-15:_ Independence Peg (Initial valuation parity baseline of ₹3.30 / $1).
  - _1949-09-18:_ Post-devaluation inflationary baseline alignment (Adjusted to ₹4.76 / $1).
  - _1966-06-06:_ Post-war structural adjustment intervention (Devalued to ₹7.50 / $1).
  - _1971-12-20:_ Smithsonian Agreement macro realignment parameter (Adjusted to ₹8.39 / $1).
