# 🚚 SwiftRoute Logistic Dashboard

> An end-to-end supply chain and fleet management analytics dashboard built using Power BI to evaluate delivery performance, optimize hub operations, and drive data-driven logistics decisions.

---

## 📌 Table of Contents

- [Overview](#-overview)
- [Business Problem](#-business-problem)
- [Dataset & Data Model](#-dataset--data-model)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Dashboard Views](#-dashboard-views)
- [Business Impact](#-business-impact)
- [Key Insights](#-key-insights)
- [How to Run This Project](#-how-to-run-this-project)
- [Final Recommendations](#-final-recommendations)
- [What Makes This Project Stand Out](#-what-makes-this-project-stand-out)
- [Author & Contact](#-author--contact)

---

## 🚀 Overview

The **SwiftRoute Logistic Dashboard** is a comprehensive business intelligence solution designed to provide supply chain managers and logistics executives with granular visibility into fleet operations, driver performance, and hub efficiency.

It enables stakeholders to:
- Monitor core delivery KPIs (On-Time Delivery, CSAT, Avg Delivery Time).
- Identify bottlenecks in hub order processing.
- Track driver performance and delay rates.
- Manage fleet health (Active vs. Maintenance statuses).
- Analyze vehicle utilization by model and age.

This project simulates an enterprise-grade logistics analytics environment using advanced data modeling, DAX measures, and highly interactive UI/UX design.

---

## 🎯 Business Problem

Logistics companies face complex challenges in maintaining delivery SLAs while managing operational costs. 

Key questions this dashboard answers:
- Are we hitting our On-Time Delivery targets and maintaining customer satisfaction?
- Which hubs are over or under-utilized regarding their processing capacity?
- Who are our top-performing drivers, and who is contributing most to delayed deliveries?
- What is the operational status of our fleet, and which vehicle types handle the most volume?
- How does delivery performance fluctuate month-over-month?

---

## 📂 Dataset & Data Model

The dataset consists of structured logistics data modeled in a robust **Star Schema** to ensure high performance and accurate aggregations.

**Data Model Architecture:**
- **Fact Table:** `Orders` (Order ID, Delivery Dates, CSAT, Delay Reasons, Processing Times)
- **Dimension Tables:**
  - `Hubs` (Hub ID, Name, Capacity)
  - `Drivers` (Driver ID, Name, Experience, Rating, Hire Date)
  - `Vehicles` (Vehicle ID, Model, Age, Purchase Date)
  - `Date Table` (Standard time intelligence)
  - `_Measure` & `Select Measure` (DAX calculations and dynamic slicer logic)

<p align="center">
  <img src="https://github.com/aman-theanalyst/SwiftRoute-Logistic-Dashboard/blob/main/Dashboard%20Images/Table%20Relationship.png" width="600" alt="Data Model">
</p>

Key KPIs engineered using DAX:
- **On-Time Delivery Rate (%)**
- **CSAT (%)**
- **Avg Delivery Time (hrs)**
- **MoM (Month-over-Month) variances**

---

## 🛠 Tech Stack

- **Power BI** (Data Modeling, UI/UX Design & Visualization)
- **DAX** (Complex KPI Calculations, Time Intelligence, Dynamic Measures)
- **Power Query** (Data Cleaning & Transformation)
- **Python** (for insight generation)
- **Git & GitHub** (Version Control & Portfolio Hosting)
  
---

## 📂 Project Structure

📦 SwiftRoute-Logistic-Dashboard   
┣ 📷 Dashboard Images   
┣ 📁 Dataset    
┣ 📷 Images  
┣ 📄 README.md    
┣ 📈 Python_Insights
┗ 📊 SwiftRoute_Dashboard.pbix   

---

## 🗂 Dashboard Views

The dashboard features intuitive navigation across **four core analytical layers**:

### 1️⃣ Executive Summary (Main View)
- High-level KPIs: Total Orders, On-Time Delivery Rate, CSAT, Avg Delivery Time.
- Month-over-Month performance tracking.
- Quick summary cards for total Hubs, Drivers, and Vehicles.

![Executive Summary](https://github.com/aman-theanalyst/SwiftRoute-Logistic-Dashboard/blob/main/Dashboard%20Images/Swiftboard%20Logistic%20Dashboard.png)

### 2️⃣ Hubs Overview
- Order Processed vs. Hub Capacity (Houston, Dallas, Austin, etc.).
- Hub performance ranking based on On-Time Delivery Rate.
- Daily processing hour heatmaps/bar charts.

![Hubs Overview](https://github.com/aman-theanalyst/SwiftRoute-Logistic-Dashboard/blob/main/Dashboard%20Images/Hub's%20Overview.png)

### 3️⃣ Drivers Overview
- Driver Experience vs. Performance Rating scatter analysis.
- Delayed Delivery Rate tracked by individual Driver Name.
- Individual Driver Profiles detailing deliveries, hire date, and YOE.

![Drivers Overview](https://github.com/aman-theanalyst/SwiftRoute-Logistic-Dashboard/blob/main/Dashboard%20Images/Drivers%20Overview.png)

### 4️⃣ Vehicles Overview
- Order distribution by Vehicle Model and Type (Van, Truck, Pickup).
- Live fleet status: Active vs. Maintenance.
- Vehicle utilization breakdown by Age and Vehicle Code.

![Vehicles Overview](https://github.com/aman-theanalyst/SwiftRoute-Logistic-Dashboard/blob/main/Dashboard%20Images/Vehicle's%20Overview.png)

---

## 📈 Business Impact

By utilizing this dashboard, logistics teams can:
- **Reduce operational bottlenecks** by identifying hubs that exceed capacity.
- **Improve customer satisfaction** through targeted tracking of delivery times and delay drivers.
- **Optimize fleet investments** by understanding which vehicle models carry the most load versus maintenance downtime.
- **Enhance workforce efficiency** by pinpointing drivers who need routing assistance.

---

## 📊 Key Insights

✅ **Performance Ratings Are Statistically Worthless**   
★5-rated drivers have a higher delay rate than ★1-rated drivers. Your internal evaluation system has zero correlation with what actually matters. Any routing or bonus decisions built on it are misallocating reward and volume.

✅ **Experience Makes Drivers Worse, Not Better**   
0–2 year drivers outperform 6–8 year veterans by 2.4 percentage points. This is the complacency paradox — veteran drivers are either taking shortcuts, or they've been assigned harder routes. Either way, tenure ≠ performance.

✅ **Delay Predicts Satisfaction With 100% Accuracy**   
Every single 1-star score came from a delayed order. Every 5-star score had zero delays. CSAT is not a multi-dimensional metric here — it has exactly one driver. Fix delays, and you fix everything.

✅ **The Freightliner M2 Is the Fleet's Weakest Link**   
At 17 average breakdowns per vehicle (vs 10.2 for the Mercedes Sprinter), the M2 is a financially indefensible asset. Retire it. Don't repair it.

✅ **Fleet Age Is a 3× Breakdown Multiplier**   
Vehicles over 6 years old average 20.5 breakdowns vs 6.9 for vehicles under 2 years. The fleet is aging into a compounding crisis — 18 vehicles are in the 4–6 year high-risk band and aging up.

✅ **May–June 2024 Revealed a Worsening Seasonal Pattern**   
The network hit 23.2% delays in June 2024 — up from 18.6% in February. Year-over-year, Q2 2024 was 10% worse than Q2 2023. The underlying deterioration is accelerating, not stable.

✅ **Faster Hub Processing Causes More Delays**   
The fastest-processing hubs have the highest delay rates. Speed at the hub creates downstream sorting errors and misroutes. The operation is optimizing the wrong metric at the hub level.

✅ **The 35.8-Hour Average Hides a Bimodal Crisis**   
Deliveries cluster into two groups: fast (6–24 hrs) and slow (24–72 hrs). P99 is 114 hours — nearly 5 days. A single SLA is being applied to what are functionally two very different service products.

✅ **High-Volume Drivers Perform Better Than Low-Volume Ones**   
The most-loaded drivers have lower delay rates. Volume isn't the problem. Skill is. Stop protecting underperformers by redistributing their load — concentrate volume on your top performers.

✅ **Dallas Fails Across Every Single Delay Category**    
Controlling for volume, Dallas leads or ties for the most delays in 9 of 10 failure categories. This isn't a volume problem — it's a broad-spectrum operational breakdown requiring a full intervention, not a targeted fix.

---

## ▶ How to Run This Project

1. Clone the repository:
```bash     
git clone [https://github.com/aman-theanalyst/SwiftRoute-Logistic-Dashboard.git](https://github.com/aman-theanalyst/SwiftRoute-Logistic-Dashboard.git)
```
2. Open the `.pbix` file in Power BI Desktop.     
3. **Interact with the Dashboard:** - Use the **left-hand navigation pane** to switch between Hubs, Drivers, and Vehicles.
   - Use the **Year and Month slicers** to observe temporal trends.
   - Hover over visuals to view custom tooltips.     

---

## 💡 Final Recommendations

- **Institute a Total Fleet Lifecycle Management Programme (Critical)**    
The fleet is in a self-compounding reliability crisis. 26.7% offline — nearly 3× the industry standard of 8–10%. Retire the Freightliner M2 immediately (17.0 avg breakdowns vs 10.2 for Mercedes Sprinter). Establish a hard lifecycle policy: preventive service at Year 4, replacement evaluation at Year 5. Projected impact: −2.0 to −2.5pp delay rate.

- **Rebuild the Driver Performance Architecture from the Ground Up (Critical)**    
The performance rating system is statistically invalid (r ≈ 0.01). It must be replaced with an outcome-based framework — delay rate, delivery time, and CSAT as the three primary scored dimensions. Implement formal performance tiers, a 60-day coaching programme for the bottom decile, and scale the contract driver model from 2 to 8–10 drivers. Projected impact: 500–800 fewer delayed orders per year.

- **Redesign the Hub Network Around an El Paso Benchmark Model (High Priority)**
The fastest-processing hubs produce the highest delay rates (22.3% vs 20.5%) — the operation is optimising the wrong metric. Dallas is a single-point-of-network failure at 29.4× volume-to-capacity. Codify El Paso's practices as the network standard, deploy them at Austin, and model Dallas risk redistribution across Houston and Fort Worth. Projected impact: −1.5 to −2.0pp delay rate.

- **Reframe the Commercial Model Around Tiered SLA and CSAT-as-Revenue (Strategic)**    
The business is selling a bimodal service product (32.9% of orders deliver in 6–24h, 50.4% in 24–72h) under a single undifferentiated SLA. Introduce Express (≤24h) and Standard (≤48h) tiers with differentiated pricing. Build an LTV-based churn model around the 3,663 at-risk customers. Add P99 exception escalation (any order past 48h triggers proactive outreach). Projected impact: dual-sided revenue and retention uplift.

- **Build a Continuous Operations Intelligence System (Structural / Multiplier)**    
Without this, all gains from Recs 01–04 will revert within 18 months — because they already have. The YoY deterioration (Q2 2024 was 10% worse than Q2 2023) is proof. Deploy a real-time ops dashboard, a 12-week seasonal capacity planning cycle, a delay incident classification protocol, and a monthly executive governance cadence. This is the compounding multiplier on every other investment.   

---

## 📌 What Makes This Project Stand Out

✔ **Enterprise-Grade UI/UX:** Clean, intuitive, app-like navigation pane.  
✔ **Advanced Data Modeling:** Clean Star Schema ensuring fast query performance.  
✔ **Actionable Metrics:** KPIs directly tied to logistics profitability and SLAs.  
✔ **Dynamic Interactivity:** Custom measure slicers and cohesive cross-filtering.  

---

## 👤 Author & Contact

**Aman Singh Negi** | Data Analyst  

🔗 [GitHub](https://github.com/aman-theanalyst)  
🔗 [LinkedIn](https://www.linkedin.com/in/aman-singh-negi-482197310)

---

## ⭐ If you found this valuable, give this repository a ⭐ and connect with me!
