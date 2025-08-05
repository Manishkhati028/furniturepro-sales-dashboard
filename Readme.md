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

## 💡 Key DAX Measures

### 🎯 1. Target Status (with conditional logic)

```DAX
TargetStatus = 
SWITCH(
    TRUE(),
    [Sales] >= [Target], "Achieved",
    [Sales] >= [Target] * 0.75, "Partial",
    "Not Achieved"
)
Used to color-code salesperson performance across regions.

🧪 2. Profit After Discount (What-If simulation)
DAX
Copy
Edit
Profit After Discount = 
[Sales Amount] - ([Sales Amount] * 'Discount Parameter'[Discount %])
Tied to a slicer to dynamically show profit after applying discounts.

👥 3. RFM Score Calculation (Customer Segmentation)
DAX
Copy
Edit
RFM Score = 
VAR Recency = ...
VAR Frequency = ...
VAR Monetary = ...
RETURN
Recency + Frequency + Monetary
Used to segment customers as Loyal, At Risk, New, etc.

📁 More measures: /dax_measures/allmeasures.txt

📊 Dashboard Pages
Executive Summary – Overall sales & returns with YoY trends and KPI cards

Customer Analysis – RFM, new customers, segment contribution, scoring system

Target Dashboard – % Target achieved with conditional color logic

What-If Dashboard – Profit simulation based on discount inputs

Pareto Analysis – Dynamic % of sales from top X% of customers

🗂️ Folder Structure
bash
Copy
Edit
furniturepro-sales-dashboard/
│
├── README.md
├── Extra images/
│   └── Banner.png
├── screenshots/
│   ├── executive_summary.png
│   ├── customer_analysis.png
│   └── whatif_analysis.png
├── docs/
│   └── FurniturePro_CaseStudy.pdf
├── dax_measures/
│   ├── allmeasures.txt
│   └── allmeasurestxt.txt
├── powerbi/
│   └── Sales_dashboard.pbix
🛠 Tools & Technologies





📸 Screenshots
🧑‍💼 Executive Summary

👥 Customer Segmentation

🧪 What-If Analysis

📄 Case Study PDF
📘 Download full case study

🚀 How to Use
Clone this repository:

bash
Copy
Edit
git clone https://github.com/Manishkhati028/furniturepro-sales-dashboard.git
Open Sales_dashboard.pbix in Power BI Desktop

Replace the data source if needed and click Refresh

Interact with slicers, charts, and simulations!

✍️ Author
Manish Khati
Data Analyst | Power BI Developer | Automation Enthusiast
🔗 LinkedIn
📧 your.email@example.com