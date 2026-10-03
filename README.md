<div align="center">

# 🤖 AI Data Analyst Agent

### AI-Powered Data Analytics & Business Intelligence Platform

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?logo=python&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-App-FF4B4B?logo=streamlit&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-Visualization-3F4F75?logo=plotly&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-F7931E?logo=scikitlearn&logoColor=white)

**Upload a CSV or Excel file → get a cleaned dataset, KPIs, a dashboard, AI insights, a chat analyst, a business report and a forecast.**

</div>

---

## 📑 Table of Contents

- [Overview](#-overview)
- [Key Features](#-key-features)
- [Design Principle](#-design-principle)
- [Tech Stack](#️-tech-stack)
- [Project Structure](#-project-structure)
- [Installation](#️-installation)
- [Environment Variables](#-environment-variables)
- [Usage](#-usage)
- [System Design](#-system-design)
- [Example Questions](#-example-business-questions)
- [Future Improvements](#-future-improvements)
- [Disclaimer](#️-disclaimer)
- [Author](#-author)

---

## 📌 Overview

Business users often have raw CSV or Excel data but don't know:

- Which columns matter
- Which KPIs to calculate
- Which charts fit the data
- Which areas are performing well or poorly
- What decisions the data supports

**AI Data Analyst Agent** solves this by automatically understanding the uploaded dataset, identifying business columns, calculating KPIs, generating dashboards, producing insights, and explaining results in plain language using an LLM.

---

## ✨ Key Features

| # | Feature | What it does |
|---|---------|--------------|
| 1 | 📂 **CSV & Excel Upload** | Previews data, shape, column names and structure |
| 2 | 🧹 **Automated Data Cleaning** | Handles missing values and duplicates; numeric → median, text → mode / `Unknown` |
| 3 | 🔎 **Exploratory Data Analysis** | Column summary, missing-value summary, numeric & categorical stats, correlation matrix |
| 4 | 📅 **Date & Time Analysis** | Auto-detects date columns; extracts Year, Month, Quarter, Week, Day, Hour, etc. |
| 5 | 📊 **Business-Aware KPIs** | Detects Sales, Profit, Quantity, Discount, Region, etc. and computes relevant KPIs |
| 6 | 📈 **Intelligent Chart Selection** | Picks the right chart type based on data pattern |
| 7 | 🖥️ **Auto Dashboard** | No manual axis, chart type or aggregation selection needed |
| 8 | 🧠 **AI Business Insights** | Best / weakest segments, margin analysis, growth, discount impact, risks |
| 9 | 🤖 **LLM Analyst Explanation** | Executive summaries, recommendations, risks & opportunities |
| 10 | 💬 **Chat With Data** | Ask questions in natural language, answered from calculated facts |
| 11 | 📄 **Business Report Generator** | Downloadable Markdown report |
| 12 | 🔮 **Forecasting** | Sales, Profit and Quantity forecast using Linear Regression baseline |

### 📊 KPIs Supported

- Total Sales / Revenue
- Total Profit & Profit Margin %
- Total Orders & Average Order Value
- Total Quantity Sold
- Average Discount
- Monthly Sales / Profit Growth %
- Top Category / Product / Region / Customer
- Cost-to-Sales Ratio

### 📈 Intelligent Chart Selection

| Data Pattern | Visualization |
|---|---|
| Date + Sales | Line Chart |
| Date + Sales + Profit | Multi-Line Chart |
| Category + Sales | Column Chart |
| Product + Sales | Horizontal Bar Chart |
| Category + Sales + Profit | Grouped Bar Chart |
| Region + Category + Sales | Clustered Column Chart |
| Category Share | Donut Chart |
| Discount + Profit | Scatter Plot |
| Multiple Numeric Measures | Heatmap |
| Sales Distribution | Histogram |

### 📄 Business Report Contents

Dataset understanding · KPI summary · Dashboard explanation · Key insights · Risks & weak areas · Opportunities · Recommended actions · KPIs to monitor

### 🔮 Forecasting Outputs

Actual vs Forecast chart · Forecast table · Forecast metrics · Forecast business insights

---

## 🎯 Design Principle

> **Python calculates the numbers. The LLM explains the meaning.**

```text
Python / Pandas  →  Accurate calculations  →  Business metrics & facts  →  LLM  →  Explanation + Recommendations
```

The LLM never calculates KPIs directly. This reduces the risk of hallucinated numbers.

---

## 🛠️ Tech Stack

| Category | Tools |
|---|---|
| Language | Python |
| Data Analytics | Pandas, NumPy |
| Machine Learning | Scikit-learn (Linear Regression) |
| Visualization | Plotly |
| Web App | Streamlit |
| AI / LLM | LLM API integration (OpenRouter) |
| File Processing | OpenPyXL |
| Config / API | Requests, Python-dotenv |

---

## 📁 Project Structure

```text
AI_Data_Analyst_Agent/
│
├── app/
│   └── main.py                  # Streamlit entry point
│
├── assets/
├── data/
├── docs/
│   └── project_documentation.md
├── notebooks/
├── reports/
│
├── src/
│   ├── analysis_planner.py
│   ├── chart_planner.py
│   ├── chat_with_data.py
│   ├── data_cleaning.py
│   ├── data_loader.py
│   ├── datetime_analysis.py
│   ├── eda.py
│   ├── insights.py
│   ├── llm_insights.py
│   ├── llm_service.py
│   ├── prediction.py
│   ├── report_generator.py
│   └── visualizations.py
│
├── .gitignore
├── README.md
└── requirements.txt
```

---

## ⚙️ Installation

**1. Clone the repository**

```bash
git clone https://github.com/yashbankhele/AI_Data_Analyst_Agent.git
cd AI_Data_Analyst_Agent
```

**2. Create a virtual environment**

```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS / Linux
python3 -m venv venv
source venv/bin/activate
```

**3. Install dependencies**

```bash
pip install -r requirements.txt
```

---

## 🔐 Environment Variables

Create a `.env` file in the project root:

```env
OPENROUTER_API_KEY=your_api_key_here
OPENROUTER_MODEL=your_model_id_here
```

> ⚠️ Never commit your `.env` file or API keys to GitHub.

---

## ▶️ Usage

Run the app:

```bash
streamlit run app/main.py
```

Then in the browser:

1. Upload a CSV or Excel dataset
2. **Data Cleaning** – clean the dataset
3. **EDA** – explore the data
4. **Date & Time Analysis** – when a date column exists
5. **Dashboard** – view auto-generated visualizations
6. **AI Insights** – understand business performance
7. **Chat With Data** – ask questions
8. **AI Business Report** – generate and download
9. **Trend Prediction** – forecast future performance

---

## 🧠 System Design

```text
          ┌─────────────────────┐
          │   CSV / Excel Data  │
          └──────────┬──────────┘
                     ▼
          ┌─────────────────────┐
          │   Data Processing   │
          │   Pandas / NumPy    │
          └──────────┬──────────┘
                     ▼
          ┌─────────────────────┐
          │ Data Cleaning + EDA │
          └──────────┬──────────┘
                     ▼
          ┌─────────────────────┐
          │ KPI & Analysis Engine│
          └──────────┬──────────┘
        ┌────────────┼────────────┐
        ▼            ▼            ▼
   Dashboard      Insights    Forecasting
        └────────────┼────────────┘
                     ▼
          ┌─────────────────────┐
          │    LLM Analysis     │
          │ Explanation / Chat  │
          └─────────────────────┘
```

---

## 💡 Example Business Questions

- What is the total revenue and profit?
- What is the profit margin?
- Which category generates the most sales?
- Which product is loss-making?
- Which region is underperforming?
- Which channel performs best?
- Are discounts hurting profitability?
- Is sales performance increasing or declining?
- What should the business investigate first?

---

## 🔮 Future Improvements

- [ ] PDF report export
- [ ] Excel report export
- [ ] Automatic anomaly detection
- [ ] Advanced forecasting models
- [ ] User authentication
- [ ] Database integration
- [ ] Domain-specific templates (Sales, Inventory, HR, Finance, Marketing)
- [ ] Dashboard image export
- [ ] Multi-file comparison

---

## ⚠️ Disclaimer

This project is built for **learning, portfolio and demonstration purposes**.

- Forecasts are basic estimates, not guaranteed predictions.
- Business recommendations are based on available dataset facts and should be validated before real-world decisions.

---

## 👨‍💻 Author

**Yash Bankhele**
B.E. Artificial Intelligence & Data Science

- GitHub: [@yashbankhele](https://github.com/yashbankhele)
- LinkedIn: [yashbankhele](https://www.linkedin.com/in/yashbankhele)

---

<div align="center">

⭐ **If you find this project useful, consider giving the repo a star!**

</div>
