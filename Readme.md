![FurniturePro Banner](Extra%20images/Banner.png)

# 📊 FurniturePro & Co. – Power BI Sales & Customer Intelligence Dashboard

A complete Power BI case study built for **FurniturePro & Co.**, a fictional retail chain, focused on delivering deep insights across sales performance, customer behavior, profitability, and marketing targeting. This project highlights strong analytical storytelling using Power BI's full stack—data modeling, Power Query, advanced DAX, and dashboard design.

---

## 🚀 Project Highlights

- ✅ 5-tab interactive Power BI dashboard (Executive, Customer, Target, What-If, Pareto)
- 📈 Dynamic KPIs with YoY & MoM trend analysis
- 🔍 RFM segmentation and customer retention logic
- 🎯 Target vs Actual comparison with conditional formatting
- 🧪 What-If scenario using user-defined discounts and predicted profit
- 📊 Pareto analysis – top customers and their sales contribution
- 🧠 Bonus: Scoring logic for marketing action planning

---

## 🧠 Business Objectives

- Understand regional and segment-wise sales trends
- Compare current vs previous year performance
- Identify customer segments using RFM logic (Recency, Frequency, Monetary)
- Highlight top-performing salespersons by state & segment
- Help marketing teams identify high-value and at-risk customers

---

## 💡 Key DAX Measures Used

### 1. 🎯 Target Achievement Logic

```DAX
TargetStatus = 
SWITCH(
    TRUE(),
    [Sales] >= [Target], "Achieved",
    [Sales] >= [Target] * 0.75, "Partial",
    "Not Achieved"
)
🔹 Used to apply conditional formatting in the Target dashboard.

2. 🧪 What-If Discount Simulation
DAX
Copy
Edit
Profit After Discount = 
[Sales Amount] - ([Sales Amount] * 'Discount Parameter'[Discount %])
🔹 Enables dynamic simulation of discount impact on profitability.

3. 👥 RFM Score – Customer Segmentation
DAX
Copy
Edit
RFM Score = 
VAR Recency = ...
VAR Frequency = ...
VAR Monetary = ...
RETURN
Recency + Frequency + Monetary
🔹 Used to classify customers: Loyal, At Risk, Lost, New.

4. 📈 YoY Sales Change
DAX
Copy
Edit
YoY Sales % Change = 
DIVIDE(
    [Total Sales] - CALCULATE([Total Sales], SAMEPERIODLASTYEAR('Date'[Date])),
    CALCULATE([Total Sales], SAMEPERIODLASTYEAR('Date'[Date]))
)
🔹 Used in KPI cards for yearly comparison.

5. 🏅 Top 5 Salespersons by Segment
DAX
Copy
Edit
Top5 Salespersons = 
RANKX(
    ALLSELECTED('Salesperson'),
    [Total Sales],
    ,
    DESC
)
🔹 Enables spotlight visuals and dynamic leaderboard.