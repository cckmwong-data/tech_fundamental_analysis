# Quantimental Intelligence: Tech Sector Fundamental Dashboard & AI Anomaly Detection

This project synchronizes deep-dive fundamental analysis for Big Tech (**Google, Meta, Nvidia, Tesla**) with a **Deep Learning LSTM Autoencoder** to identify market mispricings and price anomalies.

![](image/valuation.png)

---

## The Integration: Fundamentals meet AI
Most investment tools provide either financial data or technical indicators. This project integrates both to create a high-conviction decision engine:

* **The Fundamental Core (Power BI):** Determines **Intrinsic Value** using a dynamic 10-year DCF model. It answers: *"What is this company actually worth?"*
* **The AI Layer (LSTM Autoencoder):** Detects **Price Anomalies** in Tesla (TSLA) stock (2015-2025). It answers: *"Is the current market price deviating irrationally from historical patterns?"*

**Strategic Use Case:** When the Power BI model shows a stock is undervalued, and the LSTM model flags a negative price anomaly (high reconstruction error), it signals a statistically significant **Mean Reversion** buying opportunity.

---

## 📝 Project Overview
This platform automates the end-to-end flow of financial intelligence. By scraping daily financial statements and stock prices via Python, it eliminates the "stale data" problem common in retail research. Users can interactively adjust WACC, growth rates, and risk-free rates to see real-time shifts in target prices.

## ❗ Problem Statement
* **Data Lag:** Manual financial tracking is too slow for modern markets.
* **Static Models:** Traditional "Target Prices" don't allow for personalized risk assumptions.
* **Disconnected Insights:** Fundamental health is rarely cross-referenced with algorithmic price oversight.

---

## ✨ Key Highlights
* **Automated ETL:** Python scripts & GitHub Actions refresh the entire dataset every 24 hours.
* **Dynamic Valuation:** Interactive 2-stage DCF engine with a WACC/Terminal Growth sensitivity matrix.
* **Unsupervised Learning:** LSTM Autoencoder flags anomalies when the reconstruction error (MAE) exceeds the 95th percentile.
* **Full Financial Stack:** Dedicated modules for Income Statement, Balance Sheet, and Cash Flow (including Cash Flow Bridges).

---

## 📊 Dashboard Breakdown

### 1. Intrinsic Valuation & Sensitivity
<img src="image/valuation.jpg" width="900" alt="Valuation Dashboard">
Compare **Current Price** vs. **Intrinsic Value**. Use the interactive sliders to stress-test the valuation against different economic scenarios.

### 2. Income Statement & Margin Analysis
<img src="image/IS4.jpg" width="900" alt="Income Statement Analysis">
Track revenue growth and operational leverage. Monitor how COGS, R&D, and SG&A evolve as a percentage of total revenue.

### 3. Balance Sheet & Liquidity
<img src="image/BS2.png" width="900" alt="Balance Sheet Charts">
Analyze solvency and working capital efficiency through the **Cash Conversion Cycle (CCC)** and **Quick Ratio** trends.

### 4. Cash Flow Dynamics
<img src="image/CF2.png" width="900" alt="Cash Flow Bridge">
A visual **Cash Flow Bridge** identifies the drivers of cash movement, distinguishing between organic growth and financing activities.

---

## 🛠️ Skills Demonstrated
* **Deep Learning:** Time-series anomaly detection using LSTM Autoencoders.
* **Financial Engineering:** DCF Modeling, WACC, and Terminal Value calculations.
* **Data Engineering:** Automating cloud workflows with GitHub Actions and Google Sheets API.
* **Business Intelligence:** Advanced Power BI (DAX, dynamic parameters, and UX design).

---

## ⚙️ How the Pipeline Works
1.  **Extract:** Python scripts fetch the latest 10-K/10-Q data.
2.  **Automate:** GitHub Actions triggers the ETL process daily at 00:00 UTC.
3.  **Sync:** Cleaned data is pushed to Google Sheets (handling live price formulas).
4.  **Visualize:** Power BI Service performs a scheduled refresh to update the dashboard.

---

## ⚠️ Disclaimer
*This project is for informational purposes only. The target prices and anomaly flags generated do not constitute financial advice.*
