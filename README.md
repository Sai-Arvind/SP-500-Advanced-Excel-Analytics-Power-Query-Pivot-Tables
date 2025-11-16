# 📈 S&P 500 Financial Data Analytics & KPI Model (Excel & Power Query)

## 🎯 Project Objective
The goal of this project was to transform 60,000 rows of raw, unstructured S\&P 500 stock data (Jan–Jun 2025) into a structured, analysis-ready Excel model and generate key financial performance indicators (KPIs) and analytical charts using **Power Query** and **Pivot Tables**.

---

## 🛠️ Tools & Skills Showcased

| Category | Tool/Technique |
| :--- | :--- |
| **Tooling** | **Microsoft Excel** (2016+), **Power Query** (Get & Transform Data) |
| **Language** | **M Language** (for Power Query ETL automation) |
| **Analytics** | Financial Data Cleaning, Pivot Table KPI Modeling, Time-Series Analysis (Month/Year), Business Analytics |
| **Techniques** | **Unpivot Columns**, Replace Errors, Type Conversion, Date Extraction, **Folder Consolidation** (for large datasets), Month Sorting Logic |

---

## 🏗️ Project Workflow: The End-to-End ETL Pipeline

The entire process was automated using Power Query to handle the high volume of data ($60,000+$ rows) and prepare it for reporting.

### 1. Data Cleaning Layer (Power Query ETL)
* **Consolidated** the original 60,000+ row dataset from its source format.
* **Removed** nulls, blanks, and inconsistent records.
* **Standardized** column names, formats, and data types (especially converting text-stored numbers into proper numeric fields).
* **Automated** the entire ETL pipeline using M-code steps to ensure the process is instantly refreshable for new data.

### 2. Data Transformation Layer (Structuring & Date Logic)
* **Unpivoted** cross-tabulated data into a normalized, analysis-ready table.
* **Extracted** `Year`, `Month Name`, and `Month Number` from date fields.
* **Created** a dedicated Month Sort Column to maintain the correct chronological (Jan → Dec) order in all downstream Pivot Tables.

### 3. KPI Modeling Layer (Pivot Table Analysis)
* **Built Pivot Tables** on the cleaned, consolidated data to generate financial KPIs:
    * `Opening_Month_Start` vs. `Closing_Month_End` prices.
    * Yearly-level summaries and Ticker-level performance trends.
* **Created Pivot Charts** to visualize the key market insights below.

---

## 📊 Key Financial Insights & Charts

The analysis produced four critical charts offering different perspectives on the S\&P 500 activity from January to June 2025.

### **Chart 1: Comparative Closing Price Trend (Line Chart)**
<img width="376" height="218" alt="image" src="https://github.com/user-attachments/assets/0a98465e-8afd-4f2e-9664-b43c32d70184" />

(Using a Pivot Chart filtered to the top 5 most frequent tickers, e.g., TPL, NVR, TDG, NFLX, MTD)
* **Insight:** Tracks the daily closing price movement over the six-month period, revealing distinct volatility and price ranges for high-value stocks (like NVR) compared to lower-priced counterparts. It shows how specific companies align with or deviate from the general market trend.

### **Chart 2: Total Trading Volume by Month (Bar Chart)**
<img width="1000" height="600" alt="1" src="https://github.com/user-attachments/assets/e1af27db-0334-431f-a47b-5188cffb6ccd" />


(Using a Pivot Chart summing the `volume` field by the `Month` field)
* **Insight:** Aggregates total market activity across all S\&P 500 stocks.
    * **Peak Activity:** Trading volume peaked significantly in **April (Month 4)**, indicating the highest liquidity and market interest during the period.
    * **Lowest Activity:** The market was least active in **January (Month 1)**.

### **Chart 3: Distribution of Daily Price Returns (Histogram)**
<img width="530" height="399" alt="image" src="https://github.com/user-attachments/assets/eb76c7a1-3869-43c9-9d37-ba104e81ea70" />

(Using the **Histogram tool** on a helper column calculating `(Closing - Opening) / Opening` percent change)
* **Insight:** Measures the daily volatility and overall sentiment of the market.
    * **Low Volatility:** The distribution is tightly clustered around $0\%$, typical for a mature index.
    * **Positive Drift:** The mean daily return was slightly positive ($\mathbf{+0.0764\%}$), suggesting more trading days ended with slight gains than losses.
    * **Volatility Metric:** The high standard deviation ($\mathbf{2.04\%}$) indicates that despite the tight clustering, significant price swings occurred frequently.

### **Chart 4: Distribution of Monthly Net Price Change (Box Plot)**
<img width="1000" height="600" alt="2" src="https://github.com/user-attachments/assets/aab35596-27dd-4c4d-b660-82fbfce319e3" />


(Using the **Box and Whisker** tool on a calculated difference between the **Max Closing** and **Min Opening** price for each Ticker/Month)
* **Insight:** Reveals the long-term risk and reward profile for the typical stock over monthly horizons.
    * **Worst Performance:** The median stock experienced the largest net loss in **March $4.09**.
    * **Strongest Rebound:** The median stock saw the largest net gain in **May $3.91**, representing a major market reversal.
    * **Outliers:** The prevalence of outliers (individual dots) highlights that even in challenging months (like March), specific stocks achieved massive gains, showcasing significant individual stock risk and opportunity.

 * **High-quality analytical charts were generated using Python (Matplotlib/Seaborn) to ensure professional, portfolio-ready visualization**
---

```
## 📂 Repository Structure

S-P-500-Advanced-Excel-Analytics-Power-Query-Pivot-Tables/
│ ├── datasets/ # Raw input financial data
│ └── sp500-companies-finance.csv # 📥 The original S&P 500 financial dataset.
│
│ ├── docs/ # Documentation and resources for the project
│ ├── power_query_etl_steps.md # 📝 Details of the data cleaning, unpivoting, and M-code transformation steps.
│ ├── kpi_and_chart_definitions.md # 📈 Definitions of KPIs (e.g., Monthly Net Change) and chart analysis.
│ └── month_sorting_logic.md # 💡 Explanation of the date/month logic for time-series integrity.
│
│ ├── reports/ # Final analysis files and deliverables
│ └── Financial_KPI_Model.xlsx # 📊 Final Excel Model: Contains the consolidated data, all Pivot Tables, and the four analytical Pivot Charts.
│ ├── README.md # 📖 Main project overview and documentation.
│
├── LICENSE # 📜 License information (e.g., MIT License).
└── .gitignore # 🚫 Git ignored files (e.g., temporary Excel files like ~$Financial_KPI_Model.xlsx).

```
---

## 🌟 About Me

Hi there! I'm **A. Sai Arvind**, a passionate Data Analyst skilled in Excel, Power Query, SQL, Python, and Business Analytics. I enjoy turning raw data into meaningful insights through clean transformations and visual storytelling.

Let’s connect!

📧 **Email:** saiarvind5081@gmail.com

🔗 **LinkedIn:** https://www.linkedin.com/in/saiarvindofficial/

🔗 **GitHub:** https://github.com/Sai-Arvind

***

🛡️ **License:** This project is licensed under the MIT License.

⭐ If you found this project useful, please give it a star! ⭐
