# ☕ Coffee Shop Business Analytics

## 📌 Overview
End-to-end Business Intelligence project analyzing coffee shop performance in New York by combining transactional, calendar, and weather data at an hourly granularity.

The objective was to generate actionable insights and move from descriptive analysis to **data-driven decision-making**.

---

## 🎯 Business Questions
- How do sales vary by time of day and day of week?
- What is the impact of weather conditions on customer behavior?
- Which product categories drive the most revenue?
- How can promotions improve performance during low-demand periods?

---

## 🧠 Data Model
- **Fact Table**: Transactions (sales, quantity, revenue)
- **Dimensions**:
  - Calendar (date, weekday, holidays)
  - Weather (temperature, conditions, precipitation)

📌 Data unified using a custom **DateTimeKey** at hourly level.

---

## 🧩 Advanced Data Modeling

### 🌦️ Daily Dominant Weather Feature
Weather data was originally recorded at an **hourly level**, making business interpretation difficult.

To address this, a derived table was created to identify the **dominant weather condition per day (5 AM – 9 PM)**.

This transformation:
- Reduces noise from hourly fluctuations  
- Enables consistent day-level comparison  
- Improves business interpretability  

➡️ This feature was key to accurately measure the real impact of weather on sales.

---

## ⚙️ Technical Stack
- **Power BI** → Data modeling & dashboarding  
- **Power Query** → Data cleaning & transformation  
- **DAX** → KPI calculations & measures  
- **Python (Pandas)** → Data validation & exploration  
- **Excel / CSV** → Raw data sources  

---

## 🔬 Data Validation (Python)

Before building the BI model, data validation was performed using Python (Pandas) to ensure data quality and consistency.

### ✔ Validations performed:
- Missing values analysis  
- Duplicate detection  
- Time coverage validation  
- Hourly granularity validation  
- Revenue consistency checks  
- Weather data integrity checks  

### 📂 Notebooks:
- [Transactions Exploration](notebooks/01_bi_project_transactions_exploration.ipynb)  
- [Calendar Exploration](notebooks/02_bi_project_calendar_exploration.ipynb)  
- [Weather Exploration](notebooks/03_bi_project_weather_exploration.ipynb)

---

## 📊 Key Insights
- ☀️ **Morning peak (7–11 AM)** drives the majority of revenue → critical for staffing optimization  
- 🌧️ **Rainy days reduce transactions by up to 50%** → major risk for revenue stability  
- ☕ **Hot beverages account for ~77% of total sales** → strong opportunity for cross-selling  
- 📍 Performance varies significantly by location → location-based strategy required  

---

## 💡 Business Impact
- Identified optimal hours for staffing and inventory planning  
- Highlighted weather as a key external driver of demand  
- Suggested targeted promotions during low-demand periods  
- Built a **simulation model** to estimate potential revenue uplift  

---

## 🎮 Business Simulation

To move beyond descriptive analytics, a simulation model was built to test the impact of targeted promotions.

### 🧪 Scenario Tested
- Coffee + Bakery bundle  
- Bakery discount: **50%**  
- Customer adoption rate: **25%**  
- Context: **Rainy days & Weekends (low-demand periods)**  

### 📊 Results
- Current Revenue: **28.7K**  
- Revenue with Promotion: **30.4K**  
- Incremental Revenue: **+1.7K**  
- Revenue Increase: **~6%**  

➡️ This demonstrates how targeted promotions can mitigate demand drops and improve overall performance.

---

## 📸 Dashboard Preview

Interactive dashboards were built to explore performance across time, location, weather, and product categories.

### Overview Dashboard
![Overview](images/executive_manager_dashboard.png)

### Weather & Holidays Impact Analysis
![Weather](images/weather_and_holidays_impact_dashboard.png)

### ☀️ Hell's Kitchen – Clear Day
![Clear Day](images/No_holiday_and_clear_day_in_hells_kitchen.png)

### 🌧️ Hell's Kitchen – Rainy Day
![Rainy Day](images/No_holiday_and_rainy_day_in_hells_kitchen.png)

➡️ This comparison highlights how identical business conditions can lead to significantly different outcomes due to weather.

---

## 📁 Project Structure
- powerbi/ → Power BI dashboard (.pbix)  
- notebooks/ → Python analysis  
- images/ → Dashboard screenshots  
- docs/ → Project documentation
- data/ → Raw datasets used for analysis (transactions, weather, calendar)
---

## 🔗 Author
**Avi Kohane**  
Data Analyst | BI Enthusiast  
