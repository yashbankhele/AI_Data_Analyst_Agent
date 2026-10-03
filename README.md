
# 🤖 AI Data Analyst Agent

### AI-Powered Data Analytics & Business Intelligence Platform

**Developed by Yash Bankhele**

An intelligent data analytics web application built with **Python, Streamlit, Pandas, Plotly, Scikit-learn, and LLM integration**.

The AI Data Analyst Agent allows users to upload CSV or Excel datasets and automatically perform **data cleaning, exploratory data analysis, KPI analysis, dashboard generation, AI-powered insights, conversational data analysis, business reporting, and basic forecasting**.

---

## 👨‍💻 Developer

**Yash Bankhele**

- GitHub: https://github.com/yashbankhele
- Project Repository: https://github.com/yashbankhele/AI_Data_Analyst_Agent

---

## 📌 Project Overview

Business users often have raw CSV or Excel data but may not know:

- Which columns are important
- Which KPIs should be calculated
- Which visualizations are appropriate
- Which business areas are performing well
- Which areas need improvement
- What decisions can be taken from the data

The **AI Data Analyst Agent** addresses this problem by automatically understanding the uploaded dataset, identifying important business columns, calculating meaningful KPIs, generating dashboards, producing business insights, and explaining the results using an LLM.

---

## ✨ Key Features

### 📂 1. CSV & Excel Upload

Upload datasets in:

- CSV format
- Excel format

The application automatically displays:

- Dataset preview
- Dataset shape
- Column names
- Data structure

---

### 🧹 2. Automated Data Cleaning

The application detects and handles:

- Missing values
- Duplicate rows
- Numeric columns
- Text columns
- Data inconsistencies

Missing numeric values are handled using **median values**, while text values are handled using **mode or `Unknown`**.

---

### 🔎 3. Exploratory Data Analysis

Automatically generates:

- Dataset shape
- Column summary
- Missing-value summary
- Numerical statistics
- Categorical summaries
- Correlation matrix

---

### 📅 4. Date & Time Analysis

Automatically detects date/time columns and generates:

- Year
- Month
- Month Name
- Quarter
- Week
- Day
- Day Name
- Hour

These features enable time-based trend and performance analysis.

---

### 📊 5. Business-Aware KPI Selection

Instead of calculating random metrics, the application identifies business-related columns such as:

- Sales
- Revenue
- Profit
- Quantity
- Discount
- Cost
- Orders
- Customers
- Products
- Categories
- Regions
- Segments
- Channels
- Dates

It can calculate KPIs such as:

- Total Sales / Revenue
- Total Profit
- Profit Margin %
- Total Orders
- Average Order Value
- Total Quantity Sold
- Average Discount
- Monthly Sales Growth %
- Monthly Profit Growth %
- Top Category
- Top Product
- Top Region
- Top Customer
- Cost-to-Sales Ratio

---

### 📈 6. Intelligent Chart Selection

The application automatically selects suitable charts based on the dataset.

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

This allows the dashboard to adapt to different datasets automatically.

---

### 📊 7. Automatic Dashboard Generation

The dashboard is generated based on the structure and business meaning of the uploaded dataset.

The user does not need to manually select:

- X-axis
- Y-axis
- Chart type
- Aggregation

The application uses business logic and chart intelligence to determine suitable visualizations.

---

### 🧠 8. AI-Powered Business Insights

The application generates insights such as:

- Best-performing category
- Weakest region
- Top-performing product
- Low-profit products
- Profit margin analysis
- Sales growth analysis
- Discount impact
- Business risks
- Improvement opportunities

---

### 🤖 9. LLM-Powered Analyst Explanation

The LLM converts calculated data into understandable business language.

It can generate:

- Executive summaries
- KPI explanations
- Dashboard explanations
- Risks and opportunities
- Business recommendations
- Improvement suggestions

### Important Design Principle

> **Python calculates the numbers. The LLM explains the meaning.**

The LLM is not responsible for directly calculating KPIs.

---

### 💬 10. Chat With Data

Users can ask natural-language questions such as:

- Why is profit low?
- Which category should I focus on?
- Which region is weak?
- Which product is loss-making?
- How can the business improve sales?
- What business decision should be taken first?

The LLM responds using calculated dataset facts and summaries.

---

### 📄 11. AI Business Report Generator

The application can generate a downloadable business report containing:

- Dataset understanding
- KPI summary
- Dashboard explanation
- Key insights
- Risks and weak areas
- Opportunities
- Recommended actions
- KPIs to monitor

The report can be downloaded as a Markdown file.

---

### 🔮 12. Sales, Profit & Quantity Forecasting

The application performs basic forecasting using monthly aggregated data.

It can forecast:

- Sales
- Profit
- Quantity

The current forecasting implementation uses **Linear Regression** as a baseline model.

The application provides:

- Actual vs Forecast visualization
- Forecast table
- Forecast metrics
- Forecast business insights

---

# 🛠️ Tech Stack

### Programming
- Python

### Data Analytics
- Pandas
- NumPy

### Machine Learning
- Scikit-learn
- Linear Regression

### Visualization
- Plotly

### Web Application
- Streamlit

### AI / LLM
- LLM API Integration

### File Processing
- OpenPyXL

### API / Configuration
- Requests
- Python-dotenv

---

# 📁 Project Structure

```text
AI_Data_Analyst_Agent/
│
├── app/
│   └── main.py
│
├── assets/
│
├── data/
│
├── docs/
│   └── project_documentation.md
│
├── notebooks/
│
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
````

---

# ⚙️ Installation

## 1. Clone the Repository

```bash
git clone https://github.com/yashbankhele/AI_Data_Analyst_Agent.git
```

## 2. Navigate to the Project

```bash
cd AI_Data_Analyst_Agent
```

## 3. Create a Virtual Environment

### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

### macOS / Linux

```bash
python3 -m venv venv
source venv/bin/activate
```

## 4. Install Dependencies

```bash
pip install -r requirements.txt
```

---

# 🔐 Environment Variables

Create a `.env` file in the project root:

```env
OPENROUTER_API_KEY=your_api_key_here
OPENROUTER_MODEL=your_model_id_here
```

> ⚠️ Never upload your `.env` file or API keys to GitHub.

---

# ▶️ Run the Application

Start the Streamlit application:

```bash
streamlit run app/main.py
```

The application will open in your browser.

---

# 🚀 How to Use

1. Launch the Streamlit application.
2. Upload a CSV or Excel dataset.
3. Open **Data Cleaning** and clean the dataset.
4. Explore the dataset using **EDA**.
5. Perform **Date & Time Analysis** when required.
6. Open **Dashboard** to view automatically generated visualizations.
7. Open **AI Insights** to understand business performance.
8. Use **Chat With Data** to ask questions about the dataset.
9. Generate an **AI Business Report**.
10. Use **Trend Prediction** to forecast future performance.

---

# 🧠 System Design

The project follows a separation between **data calculation** and **AI explanation**.

```text
                ┌─────────────────────┐
                │   CSV / Excel Data  │
                └──────────┬──────────┘
                           │
                           ▼
                ┌─────────────────────┐
                │   Data Processing   │
                │   Pandas / NumPy    │
                └──────────┬──────────┘
                           │
                           ▼
                ┌─────────────────────┐
                │   Data Cleaning     │
                │       + EDA         │
                └──────────┬──────────┘
                           │
                           ▼
                ┌─────────────────────┐
                │   KPI & Analysis    │
                │      Engine         │
                └──────────┬──────────┘
                           │
             ┌─────────────┼─────────────┐
             ▼             ▼             ▼
        Dashboard       Insights      Forecasting
             │             │             │
             └─────────────┼─────────────┘
                           ▼
                ┌─────────────────────┐
                │    LLM Analysis     │
                │ Explanation / Chat  │
                └─────────────────────┘
```

---

# 🎯 Important Design Principle

```text
Python / Pandas
      ↓
Accurate calculations
      ↓
Business metrics & facts
      ↓
LLM
      ↓
Explanation + Recommendations
```

This architecture reduces the risk of allowing the LLM to independently calculate numerical KPIs.

---

# 💡 Example Business Questions

The application can help answer questions such as:

* What is the total revenue?
* What is the total profit?
* What is the profit margin?
* Which category generates the most sales?
* Which product is loss-making?
* Which region is underperforming?
* Which channel performs best?
* Are discounts affecting profitability?
* Is sales performance increasing or declining?
* What business area should be investigated first?

---

# 🔮 Future Improvements

Planned improvements include:

* PDF report export
* Excel report export
* Automatic anomaly detection
* Advanced forecasting models
* User authentication
* Database integration
* Domain-specific templates
* Sales analytics templates
* Inventory analytics templates
* HR analytics templates
* Finance analytics templates
* Marketing analytics templates
* Dashboard image export
* Multi-file comparison

---

# 📌 Project Purpose

This project was developed as a **portfolio-level AI and Data Analytics application** demonstrating practical skills in:

* Data Analytics
* Python Development
* Machine Learning
* Generative AI
* LLM Integration
* Business Intelligence
* Data Visualization
* Dashboard Development
* Forecasting
* API Integration

---

# ⚠️ Disclaimer

This project is created for **learning, portfolio, and demonstration purposes**.

Forecasting results are basic estimates and should not be treated as guaranteed business predictions.

Business recommendations are generated from available dataset facts and should be validated before real-world decision-making.

---

# 👨‍💻 Author

## Yash Bankhele

**B.E. Artificial Intelligence & Data Science**

Interested in:

* Data Analytics
* Artificial Intelligence
* Machine Learning
* Generative AI
* Python Development
* Data-driven Applications

### Connect with Me

* GitHub: [https://github.com/yashbankhele](https://github.com/yashbankhele)
* LinkedIn: [https://www.linkedin.com/in/yashbankhele](https://www.linkedin.com/in/yashbankhele)

---

⭐ **If you find this project useful, consider giving the repository a star!**

```

```
