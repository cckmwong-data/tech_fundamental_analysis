# Tech Sector Fundamental Intelligence Dashboard

![](images/cover.png)

An automated, end-to-end financial intelligence platform providing real-time fundamental analysis and intrinsic valuation for: **Google (GOOGL)**, **Meta (META)**, **Nvidia (NVDA)**, and **Tesla (TSLA)**.

---

## ## 📝 Overview
The **Tech Sector Fundamental Intelligence** project is a comprehensive equity research tool designed to democratize access to sophisticated financial modeling. It integrates live data scraping, automated ETL (Extract, Transform, Load) processes, and interactive data visualization to provide a 360-degree view of a company's financial health and market valuation.

---

## ## ❗ Problem Statement
Retail investors and analysts often struggle with:
* **Stale Data:** Financial dashboards that rely on manual updates often lag behind market movements.
* **Static Valuations:** Most platforms provide a "Target Price" without allowing users to see how changing a single variable (like a 1% shift in WACC) impacts that value.
* **Data Fragmentation:** The need to jump between different tools for valuation, margin analysis, and cash flow tracking.

**This project solves these issues by creating a unified, auto-updating environment where the user controls the narrative of the valuation.**

---

## ## ✨ Highlights
* **End-to-End Automation:** Zero-touch updates powered by GitHub Actions—data is refreshed every 24 hours without opening a single file.
* **Dynamic DCF Engine:** Features a 2-stage Discounted Cash Flow model with a built-in sensitivity matrix for WACC vs. Terminal Growth.
* **Advanced Accounting Visuals:** Includes specialized financial charts like the **Cash Flow Bridge** and **Cash Conversion Cycle** (CCC) trends.
* **Multi-Ticker Scalability:** Designed to easily add more tickers by simply updating the Python configuration.

---

## ## 🛠️ Skills Demonstrated
* **Financial Modeling:** DCF analysis, WACC calculation, Terminal Value estimation, and Ratio analysis (Liquidity, Solvency, Profitability).
* **Data Engineering:** Automating workflows with **Python** and **GitHub Actions**; managing cloud-based data in **Google Sheets**.
* **Data Visualization:** Advanced **Power BI** techniques including DAX measures, dynamic parameters, and interactive bookmarks.
* **ETL Pipeline Design:** Connecting disparate data sources into a streamlined, scheduled refresh architecture.

---

## ## ⚙️ How It Works

### ### 1. Data Architecture
* **Extraction:** Python scripts fetch the latest financial data via API/Scraping.
* **Automation:** **GitHub Actions** triggers the scripts daily.
* **Storage:** **Google Sheets** acts as a lightweight database, utilizing built-in formulas for real-time price tracking.
* **Visualization:** **Power BI Service** pulls the latest processed data from the cloud daily.

### ### 2. The Valuation Model (DCF)
The intrinsic value is calculated by forecasting Free Cash Flow (FCF) over two distinct phases:
* **Stage 1 (Years 1-5):** High-growth phase reflecting current expansion.
* **Stage 2 (Years 6-10):** Mature-growth phase as the business stabilizes.
* **Terminal Value:** Calculated at Year 10 representing perpetual value.
* **Discounting:** Uses the **Weighted Average Cost of Capital (WACC)** to bring all future cash flows to Present Value.

---

## ## 📊 Dashboard Breakdown

### ### 1. Valuation & Sensitivity
Analyzes **Intrinsic Value** vs. **Current Price**. Users can toggle Risk-Free Rates, Market Returns, and Growth Assumptions to observe real-time impacts on the target price.

### ### 2. Income Statement Analysis
Includes YoY growth tracking and margin analysis (Gross, EBITDA, Net). Highlights operational efficiency and expense ratios (R&D, SG&A) as a percentage of revenue.

### ### 3. Balance Sheet & Liquidity
Visualizes asset composition, the **Quick Ratio**, **Net Gearing**, and the **Cash Conversion Cycle** (CCC) to monitor working capital efficiency.

### ### 4. Cash Flow Dynamics
Features a **Cash Flow Bridge** identifying drivers of cash movement and an "Earnings Quality" check comparing FCF to Net Profit.

---

## ## 📂 Repository Structure
```text
├── .github/workflows/       # GitHub Action YAML for daily automation
├── scripts/                 # Python scripts for data scraping & processing
├── PowerBI/                 # .pbix files or templates
└── README.md                # Project documentation
