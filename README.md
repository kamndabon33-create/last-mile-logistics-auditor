# Last Mile Logistics Auditor

## A. Executive Summary

This project analyzes delivery performance using the Olist Brazilian E-Commerce dataset to identify the causes of delayed deliveries and their impact on customer satisfaction. By combining order, customer, review, and product data, the analysis measures delivery delays, classifies delivery performance, and identifies regions with the highest percentage of late deliveries. The results show that late deliveries are concentrated in specific states and are associated with lower customer review scores. An additional analysis of product categories highlights which types of products experience the greatest delivery delays, providing valuable insights for logistics planning and operational improvements.

---

# B. Project Links

**Notebook (Google Colab):**  
https://colab.research.google.com/drive/1PhZt6QLTGNbbhz8v-Tf4ByFO-Z3umDlU?usp=sharing

**Tableau Dashboard:**  
https://public.tableau.com/app/profile/bonfils.kamanda/viz/Kamanda_Amalitech_LastMile_Logistics_Auditor/Dashboard1?publish=yes

**Presentation (Google Slides):**  
https://docs.google.com/presentation/d/1miKPhkiQWLq36qDD-QB2bygNlXhdU_N1i58cvwF9K6s/edit?usp=sharing


---

# C. Technical Notes

## Data Cleaning

The following data preparation steps were completed:

- Loaded the required Olist datasets:
  - Orders
  - Customers
  - Reviews
  - Order Items
  - Products
  - Product Category Translation
- Converted all delivery-related date columns to datetime format.
- Joined Orders, Reviews, Customers, Order Items, and Products into a single master dataset.
- Verified that no duplicate order records were introduced during the joins.
- Calculated the delivery delay using:

```
Delivery Delay = Actual Delivery Date − Estimated Delivery Date
```

- Classified each order into one of four delivery statuses:
  - On Time
  - Late
  - Super Late
  - Not Delivered
- Removed cancelled and unavailable orders from the analysis.
- Translated Portuguese product category names into English using the provided translation dataset.
- Removed duplicate records before exporting the final Tableau dataset.

---

## Candidate's Choice

As an additional business analysis, the project includes **Average Delivery Delay by Product Category**.

This feature helps identify which product categories consistently experience longer delivery delays. Understanding these patterns enables Veridi Logistics to improve inventory planning, optimize shipping strategies, and allocate logistics resources more effectively for products that are more difficult to deliver.

---

# Project Requirements Completed

## Story 1 – Schema Builder

- Loaded multiple CSV datasets.
- Merged Orders, Customers, Reviews, Order Items, and Products.
- Verified duplicate records after joins.

---

## Story 2 – Delivery Delay Calculator

- Calculated delivery delay in days.
- Classified deliveries into:
  - On Time
  - Late
  - Super Late
  - Not Delivered
- Excluded cancelled and unavailable orders.

---

## Story 3 – Geographic Analysis

Created a visualization showing:

- Late Deliveries by State

This identifies regions with the highest delivery delays.

---

## Story 4 – Customer Sentiment Analysis

Created visualizations comparing:

- Delivery Status vs Average Review Score
- Delivery Delay Distribution

These demonstrate the relationship between delivery performance and customer satisfaction.

---

## Product Translation

Translated Portuguese product categories into English using the provided translation dataset.

---

## Tableau Dashboard

The interactive dashboard includes:

- Late Deliveries by State (Story 3 – Geographic Analysis)
- Average Review Score by Delivery Status (Story 4 – Sentiment Correlation)
- Delivery Delay Distribution (Story 2 – Delivery Performance)
- Top Delayed Product Categories (Story 5 – Translation Challenge        
Story 6 – Candidate Choice)

---

# Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Tableau Public

---

# Repository Structure

```
last-mile-logistics-auditor/
│
├── Last_Mile_Logistics_Auditor Colab.pdf
├── Last_Mile_Logistics_Auditor.ipynb
├── README.md

```

---

# Key Business Insights

- Late deliveries are concentrated in certain Brazilian states rather than occurring uniformly across the country.
- Customers who receive late deliveries generally leave lower review scores.
- Most deliveries are completed on time, but delayed deliveries have a significant impact on customer satisfaction.
- Delivery performance varies across product categories, suggesting opportunities to optimize logistics for specific product types.
- Monitoring delivery performance can help improve customer experience and operational efficiency.

---

# Future Improvements

Possible enhancements include:

- Interactive geographic heat maps
- Monthly delivery performance trends
- Delivery carrier performance comparison
- Predictive models for late delivery risk
- Executive KPI cards for real-time monitoring

---

# Author

**KAMANDA David Bonfils**

Last Mile Logistics Auditor Project
