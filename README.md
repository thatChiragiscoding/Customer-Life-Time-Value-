# 📊 Customer Lifetime Value (CLTV) Prediction Project

This project focuses on predicting Customer Lifetime Value (CLTV) using regression modeling and segmenting customers based on their potential value. It leverages real-world transactional data to identify high-value customers for strategic targeting and retention.

---

## 🎯 Objective

- Predict the **monetary value** a customer is likely to bring over time.
- Use **machine learning** (Gradient Boosting) to estimate CLTV.
- Segment customers into **Low**, **Medium**, and **High** value tiers.
- Visualize the customer distribution and insights using **Power BI**.

---

## 🧰 Tools & Technologies

- **Python**:
  - `pandas`, `numpy` – Data manipulation
  - `scikit-learn` – Model training & evaluation
  - `sqlite3` – SQL integration
- **Power BI** – Dashboarding & visualization
- **Jupyter Notebook** – Code development & documentation

---

## 📁 Dataset

- **Source**: Online retail transactional dataset
- **Fields**: `InvoiceNo`, `StockCode`, `Quantity`, `InvoiceDate`, `UnitPrice`, `CustomerID`, `Country`

---

## 🔧 Steps Followed

### 1. Data Preprocessing
- Removed null Customer IDs
- Removed canceled/negative transactions
- Converted date columns to datetime

### 2. Feature Engineering
- Calculated:
  - **Recency** – Days since last purchase
  - **Frequency** – Number of distinct invoices
  - **Monetary** – Total spend
  - **AOV (Average Order Value)** – Monetary / Frequency

### 3. Model Building
- Trained a **Gradient Boosting Regressor** on Recency, Frequency, AOV
- Evaluated model using:
  - **MAE (Mean Absolute Error)**
  - **RMSE (Root Mean Squared Error)**

### 4. CLTV Prediction & Segmentation
- Predicted CLTV for each customer
- Segmented customers into:
  - `Low`, `Medium`, and `High` CLTV tiers using `qcut`

### 5. Visualization (Power BI)
- Built an interactive dashboard with:
  - Bar chart: Customer count by CLTV segment
  - Pie chart: CLTV segment share
  - Scatter plot: Frequency vs. Monetary value
  - Histogram: Predicted CLTV distribution

---

## 📦 Deliverables

| File Name              | Description                                     |
|------------------------|-------------------------------------------------|
| `CLTV.ipynb`           | Jupyter notebook with full code and workflow    |
| `cltv_model.pkl`       | Trained ML model (serialized)                   |
| `cltv_output.csv`      | Final results with CLTV predictions & segments  |
| `cltv_project.db`      | SQLite database with cleaned transactions       |
| `CLTV.pbix`            | Power BI dashboard file                         |
| `README.md`            | Project documentation (this file)               |

---

## ✅ Result Summary

- **Trained Model**: Gradient Boosting Regressor
- **Performance**: MAE and RMSE scores printed in notebook
- **Segmentation**: CLTV classified into 3 tiers for targeted marketing

---

## 🚀 Future Improvements
- Use **XGBoost** or **LightGBM** for faster/better performance
- Incorporate **time series** modeling for future CLTV
- Include **churn probability** and customer acquisition cost

---

