# Supply Chain & Freight Analysis Dashboard (Power BI + Python)

This project is a comprehensive dashboard created to analyze freight cost, lead time, and predict future freight trends using a combination of *Power BI* and *Python* (via embedded scripts). It is structured into *four sheets*:

1. *Freight Cost Overview*
2. *Lead Time Overview*
3. *Freight Predictive Analysis*
4. *Predictive Python Visuals*

---

## Project Workflow

### 1. Data Loading & Preparation

- *Data Source: **MySQL Database*
- *Connection*: Connected directly to MySQL using Power BI's native database connector.
- *Tools Used*: Power Query for transformation and cleaning.
- *Steps Performed*:
  - Queried and loaded data from multiple MySQL tables.
  - Merged and cleaned datasets in Power Query.
  - Created relationships between:
    - Order List
    - Freight Cost
    - Product Info
    - Other dimension tables.

### 2. Calculated Columns & Measures

*Key Calculated Columns:*
- Freight Cost = Unit freight charges calculated per row.
- Lead Time = Date difference between dispatch and arrival.
- Any other derived columns used for visuals.

*Key DAX Measures:*
- Total Freight Cost
- Freight Cost per KG
- Average Lead Time
- On-Time Delivery Rate
- Warehouse Utilization
- Prediction Error Amount
- Total Predicted Freight Cost

---

## Dashboard Pages & Visuals

### *Freight Cost Overview*
Provides a high-level summary of freight costs.

*Visuals:*
- *Bar Chart*: Freight Cost by Carrier.
- *Scatter Plot*: Freight Cost vs Lead Time.
- *Bar Chart*: Freight Cost per KG by Origin Port.
- *Cards*:
  - Total Freight Cost
  - Highest Freight Cost Carrier
  - Freight Cost per KG
- *Slicers*: Carrier, Order Date, Origin Port, Plant Code, Product ID.

![WhatsApp Image 2025-04-21 at 21 57 13_34b011ec](https://github.com/user-attachments/assets/0539cf5e-1f8e-4adb-ab34-5eb4dc34b048)


---

### *Lead Time Overview*
Focuses on delivery performance and capacity.

*Visuals:*
- *Bar Chart*: On-Time Delivery % by Carrier.
- *Gauge*: Warehouse Utilization (Used vs Max).
- *Card KPIs*:
  - Average Lead Time
  - On-Time Delivery Rate
  - Minimum Lead Time Carrier
- *Slicers*: Carrier, Order Date, Origin Port, Plant Code, Product ID.

![WhatsApp Image 2025-04-21 at 21 57 14_cc2b8a6d](https://github.com/user-attachments/assets/c707e3dd-a818-4a58-b15b-41e7f94b2a94)


---

### *Freight Predictive Analysis*
Forecasts freight cost using Python and machine learning.

*Process:*
- Merged Order List and Freight Cost tables.
- Created a Python-powered table for predictive freight analysis using pandas, scikit-learn.

*Visuals:*
- *Line Chart*: Actual vs Predicted Freight Cost (Carrier-wise).
- *Table*: Carrier, Customer, Freight Cost, Predicted Cost, Prediction Error.
- *Cards*:
  - Total Predicted Freight Cost
  - Total Prediction Error
- *Slicers*: Carrier, Customer, Product ID.

![WhatsApp Image 2025-04-21 at 21 57 13_3278f747](https://github.com/user-attachments/assets/50fb8eb9-41a4-4d7e-b851-6dea5ad84930)



---

### *Predictive Python Visuals*
Displays advanced Python machine learning visuals.

*Process:*
- Used scikit-learn to create regression model (e.g., Random Forest Regressor).
- Trained on historical freight data.
- Generated outputs used in previous page’s prediction.

*Visuals:*
- Model performance and regression plot.
- Additional charts built entirely with Python visuals embedded in Power BI.

![WhatsApp Image 2025-04-21 at 21 57 13_0a685979](https://github.com/user-attachments/assets/e2e48990-70e8-4af5-aee7-beb5b40bc0af)


---

## 🛠 Tools & Technologies

- *Power BI Desktop*
- *MySQL Database*
- *SQL*
- *Power Query*
- *DAX*
- *Python (pandas, scikit-learn, matplotlib/seaborn)*
- *Machine Learning (Random Forest Regression, etc.)*

---

