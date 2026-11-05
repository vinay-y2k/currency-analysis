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

3. **Configure Credentials**
Create a `.env` file in the root directory:  
```
FRED_API_KEY=your_st_louis_fed_api_key
```

4. **Execute Pipeline**  
```
python main.py
```

## Interactive Architecture Features

* **100-Year Interactive Engine:** Fully self-contained Plotly charting system embedded directly in HTML. Works completely offline without needing an active Python kernel or server runtime.  
* **Structural Break Tracking:** Automates mathematical regime break optimizations detailing early currency pegs vs. modern floating policies.  
* **Cross-National Metrics Matrix:** Contextualizes global market data profiles tracking policy mandates, billionaire asset distributions, and systemic well-being indices across the United States and India.  



## Data Sources & Citations

This pipeline ingests and standardizes macro-financial timelines from the following primary endpoints:

* **Modern Floating Era (1973–Present):** Automated sequence ingestion from the **Federal Reserve Bank of St. Louis (FRED) API Resource Engine**. 
  * *Series ID Identifier:* `DEXINUS` (Indian Rupees to One U.S. Dollar Spot Exchange Rate).
* **Historical Sovereign Peg Era (1947–1973):** Extrapolated from historic central reserve matrices charting structural currency adjustments:
  * *1947-08-15:* Independence Peg (Initial valuation parity baseline of ₹3.30 / $1).
  * *1949-09-18:* Post-devaluation inflationary baseline alignment (Adjusted to ₹4.76 / $1).
  * *1966-06-06:* Post-war structural adjustment intervention (Devalued to ₹7.50 / $1).
  * *1971-12-20:* Smithsonian Agreement macro realignment parameter (Adjusted to ₹8.39 / $1).




