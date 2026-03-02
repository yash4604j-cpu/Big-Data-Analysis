# NYC Payroll Big Data Analytics and Machine Learning

A big data analytics project analyzing 6.7 million NYC payroll records using PySpark and machine learning.

## 📊 Overview

This project analyzes NYC Citywide Payroll Data (6.7M records) to:
- Identify high earners (top 25%) using classification models
- Predict total compensation using regression models
- Compare Logistic Regression, Decision Tree, Linear Regression, and Random Forest
- Generate CSV files for four Tableau dashboards

## 🛠️ Technologies

- PySpark 3.5
- Python 3.12
- Spark MLlib
- Tableau 2024.1
- Google Colab

## 📈 Key Results

| Model | Task | Best Score | Training Time |
|-------|------|------------|---------------|
| Logistic Regression (CV) | Classification | 96.57% AUC | 169s |
| Random Forest (CV) | Regression | R²: 0.8455 | 464s |
| Linear Regression | Regression | R²: 0.8040 | 15s |

### Feature Importance
- Base Salary: 45%
- Total OT Paid: 28% ⭐ Key Insight
- Total Other Pay: 15%
- Title: 7%
- Agency: 3%
- Borough: 2%

## 📊 Tableau Dashboards

Four dashboards are included as Tableau workbooks (.twbx):

1. **Data Quality Monitoring** - Dataset overview, KPI cards, agency rankings, trends
2. **Model Performance** - Model comparison, feature importance, best models, CV impact
3. **Business Insights** - Agency heat maps, OT analysis, job titles, yearly trends
4. **Scalability Analysis** - Training times, projections, partitions, ROI

## 📁 Reopository Structure

nyc-payroll-analytics/
├── notebooks/          # Jupyter notebooks (all code)
├── dashboards/         # Tableau workbooks (.twbx files)
├── data/              # CSV files for Tableau
├── reports/           # Project report PDF
├── requirements.txt   # Python dependencies
└── README.md         # This file



## 🔧 Technologies Used

| Component | Technology | Purpose |
|-----------|------------|---------|
| Data Processing | Apache Spark (PySpark) 3.5 | Distributed data processing |
| Programming Language | Python 3.12 | Model development |
| Machine Learning | Spark MLlib 3.5 | Scalable ML algorithms |
| Data Visualization | Tableau Desktop 2024.1 | Interactive dashboards |
| Development Environment | Google Colab | Cloud-based development |

## 📊 Dataset Description

The dataset contains 17 columns describing employee compensation:

| Column Name | Description |
|-------------|-------------|
| Fiscal Year | The fiscal year of the record |
| Payroll Number | Unique employee identifier |
| Agency Name | Name of the employing agency |
| Last Name | Employee last name |
| First Name | Employee first name |
| Mid Init | Employee middle initial |
| Agency Start Date | Date employee joined agency |
| Work Location Borough | Borough of work location |
| Title Description | Job title description |
| Leave Status | Leave status at fiscal year end |
| Base Salary | Annual base salary |
| Pay Basis | Basis of pay (per annum, per day, per hour) |
| Regular Hours | Regular hours worked |
| Regular Gross Paid | Regular pay amount |
| OT Hours | Overtime hours worked |
| Total OT Paid | Total overtime pay |
| Total Other Pay | Other payments |

## 🧠 Machine Learning Models

### Classification Models
- **Logistic Regression** (with and without cross-validation)
- **Decision Tree Classifier** (with and without cross-validation)

### Regression Models
- **Linear Regression** (with and without cross-validation)
- **Random Forest Regressor** (with and without cross-validation)

## 📈 Key Results

### Classification Performance
| Model | CV Status | AUC | Training Time |
|-------|-----------|-----|---------------|
| Logistic Regression | Without CV | 0.9651 | 169s |
| Logistic Regression | With CV | 0.9657 | 169s |
| Decision Tree | Without CV | 0.9016 | N/A |
| Decision Tree | With CV | 0.8389 | N/A |

### Regression Performance
| Model | CV Status | RMSE | R² | Training Time |
|-------|-----------|------|-----|---------------|
| Linear Regression | Without CV | $22,852 | 0.804 | 15s |
| Linear Regression | With CV | $22,852 | 0.804 | 102s |
| Random Forest | Without CV | $21,024 | 0.835 | 227s |
| Random Forest | With CV | $20,316 | 0.845 | 464s |

### Feature Importance
| Rank | Feature | Importance |
|------|---------|------------|
| 1 | Base Salary | 45% |
| 2 | Total OT Paid | 28% |
| 3 | Total Other Pay | 15% |
| 4 | Title Index | 7% |
| 5 | Agency Index | 3% |
| 6 | Borough Index | 2% |

## 📊 Tableau Dashboards

### Dashboard 1: Data Quality Monitoring
Provides an executive overview of data quality metrics including total records (6.7M), agencies (40), job titles (500+), and geographic distribution. Establishes trust in the dataset before diving into model results.

### Dashboard 2: Model Performance
Presents comprehensive model comparison with color-coded rankings, feature importance visualization, best model recommendations by use case, and cross-validation impact analysis.

### Dashboard 3: Business Insights
Translates model results into actionable insights including agency compensation heat maps, overtime analysis, top job titles treemap, and yearly compensation trends with forecasting.

### Dashboard 4: Scalability Analysis
Analyzes computational requirements including training time comparison, scalability projections for data growth, partition optimization, and ROI analysis for Tableau extracts.

## 🚀 Getting Started

### Prerequisites
- Python 3.12 or higher
- Apache Spark 3.5
- Tableau Desktop 2024.1 (for dashboards)
- Google Colab account (optional)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/nyc-payroll-analytics.git
```

