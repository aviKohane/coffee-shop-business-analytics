# ☕ Coffee Shop Analytics – Project Summary

## 🎯 Objective
The goal of this project was to analyze coffee shop performance in New York by combining multiple data sources (transactions, weather, and calendar) at an hourly level.

The objective was to generate actionable insights to support both operational and strategic business decisions.

---

## 📊 Data Sources
The analysis is based on three main datasets:

- **Transactions**: sales, quantities, revenue by product and store  
- **Weather**: hourly weather conditions (rain, temperature, etc.)  
- **Calendar**: weekdays, weekends, and holidays (federal & religious)

To ensure consistency, all datasets were aligned using a common **DateTimeKey** at hourly level.

---

## ⚙️ Data Preparation
- Data exploration and validation performed using **Python (Pandas)**  
- Data cleaning and transformation done in **Power Query**  
- Data modeling and relationships built in **Power BI**  
- Creation of calculated measures using **DAX**

Special attention was given to:
- Data quality (missing values, duplicates)  
- Time consistency (hourly granularity)  
- Alignment between datasets  

---

## 🧠 Data Model
A star schema was designed:

- **Fact table**: Transactions  
- **Dimensions**: Calendar, Weather  

A key feature of the model is the use of a **DateTimeKey** to enable precise hourly analysis and cross-dataset integration.

---

## 🧩 Advanced Data Modeling

### 🌦️ Daily Dominant Weather Feature

Weather data was originally recorded at an **hourly level**, which made it difficult to analyze its impact from a business perspective.

To address this, a derived table was created to identify the **dominant weather condition per day**.

### 🔧 Approach
- Focused on business hours (**5 AM – 9 PM**)  
- Identified the **most frequent weather condition per day**  
- Assigned a single “dominant weather” label per day  

### 🎯 Why it matters
- Reduces noise from hourly fluctuations  
- Transforms raw data into a **business-relevant indicator**  
- Enables clear comparison between operational days  

### 📊 Impact on analysis
This transformation allowed a much clearer evaluation of weather impact:

➡️ Rainy days significantly reduce customer activity  
➡️ Enables consistent comparison across locations and time  

---

## 📈 Key Insights

### ⏰ Time Analysis
- Strong revenue peak observed between **7 AM and 11 AM**  
- Morning hours are the most critical for performance  

➡️ Supports staffing and inventory optimization  

📸 Example:
![Time Analysis](/images/executive_manager_dashboard.png)

---

### ☕ Product Segmentation
- **Hot beverages represent ~77% of total sales**  

➡️ Indicates strong dependency on core products  
➡️ Opportunity for **cross-selling strategies** (coffee + pastry)

📸 Example:
![Product Segmentation](/images/product_sales_segmentation.png)

---

### 🌧️ Weather Impact (Detailed Example)

Using the dominant weather feature, we compared similar business conditions:

- Same location  
- Same holiday status  
- Different weather conditions  

📍 **Hell’s Kitchen Example**

- Clear day → ~172 transactions  
- Rainy day → ~85 transactions  

➡️ **~50% drop in customer activity**

📸 Clear Day:
![Clear Day](/images/No_holiday_and_clear_day_in_hells_kitchen.png)

📸 Rainy Day:
![Rainy Day](/images/No_holiday_and_rainy_day_in_hells_kitchen.png)

➡️ This demonstrates the **direct operational impact of weather**

---

## 🎮 Business Simulation (Promotion Strategy)

To go beyond analysis, a simulation model was built to estimate the impact of targeted promotions.
This simulation focuses on the most critical scenarios identified in the analysis (rainy days and weekends), where demand is naturally lower.

### 🧪 Scenario Tested
- Product bundle: **Coffee + Bakery**
- Bakery discount: **50%**
- Customer adoption rate: **25%**
- Context: **Low-demand conditions (Rainy days & Weekends)**

### 🎯 Objective
Evaluate whether targeted promotions can compensate for reduced demand during unfavorable conditions.

### 📊 Results
- Current Revenue: **28.7K**
- Simulated Revenue: **30.4K**
- Incremental Revenue: **+1.7K**
- Revenue Increase: **~6%**

📸 Example:
![Simulation](images/![Simulation](/images/business_simulator_dashboard.png)

### 💡 Insight
Targeted promotions during low-demand periods can significantly mitigate revenue loss and improve overall performance.

### 🚀 Business Value
- Helps decision-makers test strategies before implementation  
- Supports **data-driven marketing decisions**  
- Demonstrates potential ROI of promotions  

---

## ⚠️ Limitations

- Limited timeframe (6 months only)  
- No customer-level data  
- No pricing or promotion data  
- External factors not included (events, marketing campaigns)

---

## 🚀 Next Steps

- Integrate **customer segmentation**  
- Include **pricing and promotion data**  
- Extend dataset to full year  
- Build **predictive models (forecasting)**  

---

## ✅ Conclusion

This project demonstrates how combining multiple datasets and applying thoughtful data modeling can generate meaningful business insights.

It highlights the importance of transforming raw data into actionable information to support better decision-making.
