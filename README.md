# 📈 Wealth Control Center: AI-Enhanced Investment Ecosystem

**Automated Portfolio Management & Market Benchmarking System**

## 📖 Overview
This project is not just a spreadsheet; it is a comprehensive **financial product** engineered to solve a common problem: lack of control and clarity over personal wealth.

Developed with a **Product Manager mindset**—from technical requirement analysis to UX/UI design—this system leverages **AI tools and Google Apps Script** to transform static data into a dynamic, "Set & Forget" control center.

It integrates live data, processes it in real-time, and visualizes actionable insights to answer the most critical question: **"Am I truly in control of my financial picture, and how is my portfolio performing in real-time?"**

---

## 💡 Key Features & Capabilities

### 1. 🔮 Predictive Beta Simulator (The "What If" Engine)
Moving beyond historical data, this system looks forward.
* **Deterministic Modeling:** A simulator that translates S&P 500 fluctuations into immediate projected Profit/Loss for the portfolio.
* **Risk Forecasting:** Predicts how the portfolio will react to market scenarios *before* they happen, based on weighted Beta calculations.

### 2. 💰 True Net Worth Tracking (Real-Time Liquidity)
Most dashboards show "Paper Value." This system simulates a liquidation scenario in real-time:
* **Tax Simulation:** Automatically calculates Capital Gains Tax liability.
* **Forex Adjustment:** Adjusts for live currency exchange rates.
* **Result:** Displays the **"After-Tax Liquidity"** (Cash-in-hand value) at any given moment.

### 3. 📉 Honest Performance Benchmarking
A comparative view that normalizes performance to the **exact entry date** of each position (vs. generic YTD comparisons).
* **Triple Analysis:** USD Return vs. ILS Return vs. S&P 500 Benchmark.
* **Real Alpha:** Accurately measures if the portfolio is beating the market over the specific holding period.

### 4. 📊 Risk Management & KPI Monitor
A centralized dashboard for active risk assessment:
* **Asset Allocation:** Visual breakdown of exposure by stock and sector to prevent over-concentration.
* **Volatility Tracking:** Monitors **Drawdown** (drop from peak) and **P/E Ratios** to identify buy-the-dip opportunities and valuation risks.

### 5. 🚀 Scalability & Total Wealth View
The system is architected to be scalable beyond just the stock market. It aggregates **all asset classes**—including Pension funds, Provident funds (Gemel), and Real Estate—providing a holistic view of the user's entire financial life.

---

## 🛠️ Tech Stack
* **Core Platform:** Google Sheets (Cloud-based accessibility).
* **Automation:** Google Apps Script (GAS) for backend logic.
* **Intelligence:** LLM-assisted code generation for complex data processing.
* **Data Source:** Google Finance API (Real-time integration).

---

## ⚙️ Under the Hood: Engineering & Architecture

### 🔄 The Pivot: From V1 to V2 (Product Decision)
In the initial version (V1), I utilized **Google Apps Script** to fetch data via external JSON APIs. While technically functional, this approach proved "brittle" due to external dependencies and traffic limits.
Acting as the **Product Manager**, I made a strategic decision to prioritize **System Robustness** over complexity. I refactored the architecture to a **Native Approach** (leveraging advanced `GOOGLEFINANCE` wrappers nested within `QUERY` and `INDEX` functions). This ensured a continuous data stream with zero dependence on third-party servers.

### 🧩 Dynamic Resolution Algorithm
Visualizing historical performance against the market presented a challenge: "Dirty Data" and computational overload from thousands of data points.
To solve this, I developed a **Dynamic Resolution Mechanism**. This algorithm:
1.  **Filters anomalies** and errors in the raw data stream.
2.  **Adjusts sampling density:** It calculates the optimal number of data points to render based on the portfolio's age, ensuring smooth graph performance without crashing the calculation engine.

### ⚖️ Technical Trade-offs & Transparency
Every engineering decision comes with a cost. Here are the conscious trade-offs made for this system:
* **Latency vs. Accuracy:** Due to heavy parallel calculations of real-time metrics, users with asset-heavy portfolios might experience a slight loading delay. This was a calculated choice to guarantee data integrity over speed.
* **The "IPO Paradox":** For "young" assets (recently IPO'd) held within a long-term portfolio, historical benchmarking prior to their listing date is handled via fallback logic to maintain graph continuity.

---

### 👤 Author
**Eldar** - Industrial Engineering & Management Student.
Passionate about FinTech, Data Analytics, and Product Management.
