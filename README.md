<img width="2008" height="1648" alt="image" src="https://github.com/user-attachments/assets/912e3b3b-792a-45e8-9ace-63ae4297b6b4" /># -Smart-Supply-Chain-Analytics
An end-to-end data engineering solution that optimizes global logistics. Features a Python ETL pipeline, a Star Schema SQL warehouse, and a Random Forest model to predict late delivery risks.
 

##  Project Overview
This project is an end-to-end data engineering and analytics solution designed to optimize a global supply chain. 
I analyzed 180,000+ transaction recordsto identify delivery bottlenecks, predict late shipments using Machine Learning, and segment customers for targeted retention.

**Business Goal:** Reduce late delivery risk and improve inventory placement.

### Tech Stack:
*Python (Pandas & NumPy):** Data cleaning, feature engineering (calculating Haversine distance), and normalization.
*Machine Learning (Scikit-Learn):** Random Forest Classifier to predict late delivery risk (Accuracy: ~80%).
* SQL Server (T-SQL): Data warehousing with a Star Schema (Facts & Dimensions).
  *Azure Data Studio:Advanced SQL queries for business insights.

---

## SQL Analysis & Business Insights

1. Bottleneck Analysis 
*Business Question:Which shipping modes have the highest risk of being late, and does distance play a role?
> Insight: 'Standard Class' accounts for 60% of all late deliveries, specifically on routes exceeding 500km.
><img width="2008" height="1648" alt="image" src="https://github.com/user-attachments/assets/b9225f52-ce97-4e2f-a6b3-ec2adb6c28fc" />


 


 

### 2. Regional Product Performance 
Business Question:What are the top 3 selling products in every region?*
> Insight: Western Europe and Central America have completely different top-selling categories, suggesting a need for regional inventory customization.
> <img width="2056" height="1672" alt="image" src="https://github.com/user-attachments/assets/3eedcbe2-8e5a-49e9-a660-58faaea178fa" />


 

### 3. High-Value Customer Churn Risk (Query 15)
Business Question:Who are our VIP customers (Spent > $5000) and are they receiving good service?
> Insight: Identified 20 VIP customers who have experienced 3+ late deliveries and are at high risk of churning.
> <img width="2055" height="1699" alt="image" src="https://github.com/user-attachments/assets/8f26628e-0e1f-4e03-b8a6-b41a3c1c8803" />


 

---

##  Data Architecture (Star Schema)
To optimize query performance, I normalized the raw data into a Star Schema:
* Fact_Supply_Chain: Contains 180k+ transactional rows (Order ID, Dates, Sales, Risk Scores).
* Dim_Customers:*Customer PII (Name, City, Segment).
  *Dim_Products: Product details (Category, Price, Card ID).

##  How to Run
1.  Python: Run `Supply_Chain_ETL.ipynb` to clean raw data and generate the ML risk scores.
 2. Analysis: Execute ` Supply Chain SQl queries ` to reproduce the insights above.
