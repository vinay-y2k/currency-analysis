\# USD to INR 100-Year Continuum \& Macro Analysis Terminal



An interactive macroeconomic engine exploring USD/INR exchange rate trajectories (1947–2050). The framework optimizes a 3-regime piecewise global trend break structure and models future horizons using ARIMA upward drift vectors and seasonal Prophet curves.



\## Local Installation \& Setup



1\. \*\*Clone the Repository\*\*

&#x20;  ```bash

&#x20;  git clone <your-github-repo-url>

&#x20;  cd <repository-folder-name>

&#x20;  ```



2\. \*\*Configure Environment \& Dependencies\*\*

&#x20;  ```bash

&#x20;  python -m venv venv

&#x20;  source venv/bin/activate  # Windows: .\\venv\\Scripts\\activate

&#x20;  pip install -r requirements.txt

&#x20;  ```



3\. \*\*Configure Credentials\*\*

&#x20;  Create a `.env` file in the root directory:

&#x20;  ```text

&#x20;  FRED\_API\_KEY=your\_st\_louis\_fed\_api\_key

&#x20;  ```



4\. \*\*Execute Pipeline\*\*

&#x20;  ```bash

&#x20;  python main.py

&#x20;  ```



\## Interactive Architecture Features

\* \*\*100-Year Interactive Engine:\*\* Fully self-contained Plotly charting system embedded directly in HTML. Works completely offline without needing an active Python kernel or server runtime.

\* \*\*Structural Break Tracking:\*\* Automates mathematical regime break optimizations detailing early currency pegs vs. modern floating policies.

\* \*\*Cross-National Metrics Matrix:\*\* Contextualizes global market data profiles tracking policy mandates, billionaire asset distributions, and systemic well-being indices across the United States and India.



