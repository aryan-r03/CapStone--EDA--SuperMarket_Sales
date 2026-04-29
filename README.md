# 🛒 Supermarket Sales Analysis — Capstone Project

A comprehensive exploratory data analysis (EDA) and machine learning project on supermarket sales data, covering data cleaning, statistical analysis, multi-dimensional visualizations, and predictive modelling.

---

## 📁 Project Files

| File | Description |
|------|-------------|
| `CapStone.ipynb` | Main Jupyter Notebook with all analysis and visualizations |
| `CapStone.py` | Python script version of the notebook |
| `supermarket_sales.csv` | Raw dataset (1,000 transactions) |

---

## 📊 Dataset Overview

The dataset contains **1,000 supermarket transactions** across three branches and cities with the following columns:

| Column | Description |
|--------|-------------|
| `invoice_id` | Unique transaction identifier |
| `branch` | Store branch (A, B, C) |
| `city` | City of the branch (Yangon, Mandalay, Naypyitaw) |
| `customer_type` | Member or Normal customer |
| `gender_customer` | Customer gender |
| `product_line` | Product category (6 categories) |
| `unit_cost` | Price per unit |
| `quantity` | Number of items purchased |
| `revenue` | Total transaction revenue |
| `date` | Transaction date |
| `time` | Transaction time |
| `payment_method` | Payment method (Cash, Ewallet, Credit card) |
| `rating` | Customer satisfaction rating |
| `gross_income` | Gross income from transaction |

---

## 🔍 Analysis Modules

### 1. Outlier Detection & Removal
- Applied the **IQR (Interquartile Range)** method on the `revenue` column
- Visualized before/after distributions using **boxplots**

### 2. Revenue Distribution Analysis
- Handled missing values using **mean imputation**
- Visualized distribution via **histogram** and **boxplot**

### 3. Category-wise Performance
- Aggregated total sales revenue by `product_line`
- Visualized with a **bar chart** and **pie chart** to show both absolute and proportional performance

### 4. Branch Performance Analysis
- Compared branches on **total revenue**, **average transaction value**, and **customer footfall**
- Displayed using grouped **bar charts**

### 5. Payment Method Analysis
- Analyzed transaction count and revenue contribution per payment method
- Visualized with a **pie chart** (share) and **bar chart** (revenue)

### 6. Peak Shopping Hours
- Extracted `hour` and `day_name` from datetime columns
- Identified high-activity windows via a **line chart** (hourly trends) and a **day × hour heatmap**

### 7. Gender vs Product Line Spending
- Compared male and female spending patterns across all product lines
- Visualized with **grouped bar charts** (total & average) and a **spending heatmap**

### 8. City-wise Business Insights
- Compared cities on total revenue, product line preferences, and customer type distribution
- Visualized with **multi-panel bar charts**

### 9. High vs Low Quantity Transaction Analysis
- Segmented transactions by quantity (above/below median)
- Compared **average revenue** and **product mix** between segments using bar and stacked bar charts

### 10. Revenue Prediction (Linear Regression)
- **Features:** `unit_cost`, `quantity`, `rating`
- **Target:** `revenue`
- 80/20 train-test split, trained with **scikit-learn's LinearRegression**
- Evaluated using **R² Score** and **RMSE**
- Visualized with an **Actual vs Predicted scatter plot**

---

## ⚙️ Requirements

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

| Library | Purpose |
|---------|---------|
| `pandas` | Data loading and manipulation |
| `numpy` | Numerical operations |
| `matplotlib` | Core plotting |
| `seaborn` | Statistical visualizations |
| `scikit-learn` | Machine learning model and evaluation |

---

## 🚀 How to Run

**Jupyter Notebook:**
```bash
jupyter notebook CapStone.ipynb
```

**Python Script:**
```bash
python CapStone.py
```

> **Note:** Ensure `supermarket_sales.csv` is in the same directory as the script, and update the file path in the `pd.read_csv(...)` call if needed.

---

## 📈 Key Findings

- **Revenue distribution** is approximately normal with a few high-value outliers removed via IQR.
- **Branch performance** is relatively balanced, with minor differences in footfall and average transaction value.
- **Peak shopping hours** cluster around mid-morning and early evening, visible in the day-hour heatmap.
- **Gender spending** shows category-specific preferences between male and female customers.
- **Linear Regression model** achieves a strong R² score, with `unit_cost` and `quantity` being the primary revenue drivers.

---

## 👤 Author

Capstone Project — Data Analysis & Machine Learning  
*Built with Python, pandas, matplotlib, seaborn, and scikit-learn*
