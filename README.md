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
- [Research Questions](#-research-questions)
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
- **Figma / PowerPoint** (Custom background and UI layer design)
- **Git & GitHub** (Version Control & Portfolio Hosting)
  
---

## 📂 Project Structure

📦 SwiftRoute-Logistic-Dashboard   
┣ 📷 Dashboard Images   
┣ 📁 Dataset    
┣ 📷 Images  
┣ 📄 README.md    
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

## ❓ Research Questions

### 1️⃣ Which hubs are the most efficient?
Facilities like San Antonio and Fort Worth lead in on-time delivery percentages, while larger hubs like Houston show capacity strains.

### 2️⃣ What is the health of our fleet?
Tracking the percentage of vehicles in maintenance (e.g., ~26% in selected periods) allows for proactive fleet scaling and maintenance scheduling.

### 3️⃣ Which vehicles do the heavy lifting?
The Freightliner M2 consistently handles the highest breakdown of total orders and overall volume.

### 4️⃣ Are experienced drivers performing better?
Scatter plot analysis visualizes the correlation between years of experience and 5-star performance ratings, highlighting training opportunities.

---

## 📊 Key Insights

✅ **Hub Capacity vs. Efficiency:** Houston Hub processes a massive volume of orders but has a lower On-Time Delivery rate (~79.7%) compared to the San Antonio Hub (~82.8%), indicating a need for load redistribution or routing optimization.   

✅ **Fleet Utilization:** The Freightliner M2 handles the absolute majority of orders (153 breakdown), far outpacing other models. However, nearly 26.6% of the fleet can be tied up in maintenance in given months, risking capacity crunches.   

✅ **Driver Delay Discrepancies:** A handful of drivers (e.g., John Moore, Daniel Davis) show delayed delivery rates exceeding 40%. Targeted route re-evaluation for these specific drivers could instantly boost overall CSAT.   

✅ **Consistent Service Levels:** The overall CSAT hovers around a healthy 85%, tightly correlated with the ~80% On-Time Delivery rate, proving that speed and predictability are the primary drivers of customer satisfaction.

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

- **Balance the Load:** Reroute some overflow orders from the Houston Hub to nearby facilities to improve the region's overall on-time delivery rate.
- **Proactive Fleet Maintenance:** With over a quarter of the fleet occasionally in maintenance, conduct preventative checks on the heavily utilized Freightliner M2s to prevent unexpected breakdowns.
- **Targeted Driver Support:** Implement a coaching or routing-assistance program for the bottom 10% of drivers contributing to the highest delayed delivery rates. 

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
