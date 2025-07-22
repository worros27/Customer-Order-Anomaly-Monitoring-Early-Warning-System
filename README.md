# Customer Order Anomaly Monitoring & Early Warning System

This project builds an end-to-end anomaly detection pipeline to identify behavioral shifts among B2B customers and flag products with potential drop-off patterns. It is based on real-world sales data from a packaging distributor.

## 📌 Objective

Detect customers with declining purchase behavior and identify products they stopped buying recently, to support timely sales intervention.

## 🧰 Tools

- Python (Pandas, Scikit-learn)
- SQL / Excel for data preparation
- [Optional] Tableau for visualization

## 🔧 Modules

### 1. Monthly Customer Behavior Table (Data Aggregation)
- Constructed a `Customer x Month` table with metrics like SKU count, order count, and total amount.
- Output: `Cleaned_Monthly_Customer_Behavior.csv`

### 2. Anomaly Detection (Isolation Forest)
- Trained an Isolation Forest model to flag behavioral anomalies based on monthly patterns.
- Output: `customer_behavior_tags.csv`, `anomaly_customer_summary.csv`

### 3. Drop-off Product Identification
- For anomaly-only customers, identified products with ≥2 months of purchase history but no repurchase since Feb–July 2025.
- Output: `dropoff_anomaly_only_filtered.csv`

## 📁 Project Structure

See folder layout for:
- `data/` – Input/output CSVs
- `notebooks/` – Python modeling scripts
- `outputs/` – (Optional) charts or Excel reports
- `README.md` – This documentation

## ✨ Outcome

This system supports sales and account managers to:
- Detect churn risks early
- Understand product-level drop-offs
- Take timely action to retain key clients

## 🔄 Future Work

- Excel report auto-generation (Module 4)
- Tableau dashboards (Module 5)
