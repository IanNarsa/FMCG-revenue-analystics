# 📊 FMCG Revenue & Profitability Analytics Portfolio

[![Role: BI / Revenue Analyst](https://img.shields.io/badge/Role-BI%20%2F%20Revenue%20Analyst-blue.svg)](#)
[![Tech: SQL & Python](https://img.shields.io/badge/Tech-SQL%20%7C%20Python%20%7C%20Looker%20Studio-orange.svg)](#)
[![Industry: FMCG / Retail](https://img.shields.io/badge/Industry-FMCG%20%2F%20Retail-green.svg)](#)

> **Business Case Objective:** Evaluate 2024 sales performance across 10 regions, 25 SKUs, and 20 distributor partners — integrating three datasets (transactions, regional targets, and distributor stock data) — to determine whether revenue targets were realistic, identify key revenue drivers, detect distributor operational risks, and deliver data-backed strategic recommendations to senior management.

---

## 📈 Executive Dashboard

In this project, I acted as a **Lead BI Analyst** for an Indonesian FMCG company operating across **10 regions**, **25 SKUs** (5 categories), **3 sales channels**, and **20 distributor partners**. The analysis integrates three datasets to answer four critical management questions: Are targets realistic? What drives revenue? Are distributors healthy? And what is actually causing the performance gap?

### **Key Metrics & Impact Summary**
* **National Target Achievement 2024:** `86.17%` — all 10 regions clustered in a narrow band of **85.2%–86.8%**, strongly suggesting the gap stems from baseline target-setting, not local execution failures.
* **Distributor Channel Revenue Share:** `55.4%` of total revenue — yet all three channels (Distributor, Modern Trade, General Trade) carry **practically identical gross margins (~18.7–18.9%)**, meaning channel mix decisions should be driven by volume strategy, not margin assumptions.
* **Core SKU Concentration (Pareto 80/20):** **14 out of 25 SKUs** generate 80% of revenue — these are the critical products to prioritize for stock availability and trade marketing investment.
* **Distributor Health:** All **20 distributors** maintain a healthy Sell-Through Rate (>80%), but a **recurring seasonal inventory build-up** was identified in January, October, and November — a systemic pattern, not isolated incidents.
* **Cross-Dataset Correlation Finding:** **No strong correlation** was found between distributor health and regional target achievement — confirming the revenue gap is more attributable to market demand conditions or target calibration, not distribution chain failures.


## 🔍 Core Insights & Strategic Impact

### 1. **Revenue Target Calibration Gap**
* **The Finding:** National target achievement stood at **86.17%**, with all 10 regions clustering tightly in a **85.2%–86.8%** band. The near-identical underperformance across all regions — regardless of local conditions — strongly indicates the gap originates from an overly aggressive baseline target, not from execution failures at the regional level.
* **Strategic Action:** Reassess the 2025 target baseline using actual 2024 performance as the reference point. This prevents disproportionate sales pressure on field teams and enables more credible regional commitments.

### 2. **Channel Margin Parity (Data Overturns Assumption)**
* **The Finding:** Despite Distributors commanding **55.4% of revenue**, all three channels (Distributor, Modern Trade, General Trade) carry **virtually identical gross margins (~18.7%–18.9%)**. The commonly held assumption that General Trade is more profitable per-unit is not supported by the data.
* **Strategic Action:** Channel mix decisions should be redirected to **volume growth strategy** — not margin optimization arguments. Any proposal to shift channel mix must now justify itself on reach, scalability, or cost-to-serve, not on margin assumptions.

### 3. **Core SKU Concentration & Stock Priority**
* **The Finding:** Only **14 out of 25 SKUs** drive 80% of total revenue (Pareto). These core products are the most critical to protect from stockout risk, especially given the identified seasonal inventory build-up patterns.
* **Strategic Action:** Prioritize **safety stock planning** for the 14 Core SKUs. Lost sales risk from stockout on these products carries the highest revenue impact across all channels and regions.

### 4. **Seasonal Distributor Inventory Build-Up**
* **The Finding:** All 20 distributor partners maintain a healthy Sell-Through Rate (>80%), but a **recurring seasonal over-stocking pattern** was detected in **January, October, and November**. This is a systemic, multi-year cycle — not a one-off incident — indicating a structural issue in delivery scheduling or demand forecasting.
* **Strategic Action:** Review inbound stock delivery schedules in the months preceding January and the October–November window to reduce holding costs from excess inventory accumulation.

---

## 🗂️ Project Repository Map

Navigate through the code files that power these insights:

* 📁 **[data/](/data/)**
  * [`fmcg_sales_2024.csv`](/data/fmcg_sales_2024.csv): The primary transactional dataset — 1,500+ records containing units sold, pricing, costs, sales channels, customer types, and regional breakdowns.
  * [`distributor_performance_2024.csv`](/data/distributor_performance_2024.csv): Monthly distributor-level sell-through data (STD/STT quantities and ending inventory) across multiple regions and distributor IDs, used to evaluate channel efficiency and inventory health.
  * [`sales_target_2024.csv`](/data/sales_target_2024.csv): Regional monthly revenue and unit targets for 2024, used as benchmarks to measure actual vs. target performance gaps.

* 📁 **[notebook/](notebook/)**
  * [`FMCG_Data_Analytics.ipynb`](/notebook/FMCG_Data_Analytics.ipynb): The core Python analytics engine. Features data cleansing, missing value diagnostics, Pareto (80/20) calculations, distributor performance analysis, target vs. actual benchmarking, product performance matrices, and predictive sales forecasting models.
  * [`Customer_City_Segmentation.ipynb`](/notebook/Customer_City_Segmentation.ipynb): A dedicated notebook for segmenting customers based on city-level metrics, identifying regional purchasing behaviors, and demographic-driven revenue patterns.


* 📁 **[docs/](/docs/)**
  * [`business_case_study.md`](/docs/business_case_study.md): A business advisory report outlining executive summaries, regional diagnostics, and portfolio optimization.

---

## ⚡ Technical Tooling & Skills Demonstrated

* **Data Wrangling & Descriptive Analytics:** `Python (Pandas, NumPy)` for dataset diagnostics, missing values audits, and multi-dimensional aggregations.
* **Statistical Modeling & Forecasting:** `Scikit-Learn (LinearRegression)` for calculating trend-based seasonal revenues.
* **Exploratory Data Visualization:** `Matplotlib` and `Seaborn` to plot margin distributions, customer segment charts, and SKU matrices.
* **Strategic Communication:** Translating deep technical data charts into business language (Pareto rule, BCG-style matrix classifications, operational recommendations).

---

## 💼 Let's Connect!
I am a **Data & BI Analyst** passionate about driving business growth through numbers. I specialize in bridging the gap between raw data pipelines and senior management decisions. 

* **Like what you see in the code?** Check out my core logic inside the notebook: **[`FMCG_Data_Analytics.ipynb`](/notebook/FMCG_Data_Analytics.ipynb)**.
* **Looking to hire a result-oriented analyst?** Let's discuss how I can bring these analytical frameworks to optimize your business! Reach out to me via email or LinkedIn.

[`🛜 My Linkedin Septian Narsa Putra`](https://linkedin.com/in/septian-narsa-putra)

[`📧 My e-mail iannarsa@gmail.com`](iannarsa@gmail.com)