# ⛽ Fuel Efficiency Optimization Dashboard – Power BI DMAIC Case Study

### 🎯 Objective
This project demonstrates a structured approach to solving business challenges in Power BI by applying a **hybrid methodology** that combines two powerful frameworks:  
- **DMAIC (Define – Measure – Analyze – Improve – Control)** from Continuous Improvement  
- **CRISP-DM (Business Understanding – Data Understanding – Data Preparation – Modeling – Evaluation – Deployment)** from Data Science and Data Mining  

The aim is to use **continuous improvement principles** within **data analytics** to:
- Clearly define the business problem and stakeholder needs (**Define / Business Understanding**)  
- Measure and understand key data sources (**Measure / Data Understanding**)  
- Analyze and model data to uncover inefficiencies (**Analyze / Data Preparation & Modeling**)  
- Implement and evaluate operational improvements (**Improve / Evaluation**)  
- Deploy and sustain data-driven monitoring processes (**Control / Deployment**)  

This hybrid approach ensures both **analytical structure** and **process discipline**, turning business data into actionable insights.  

The case study focuses on **reducing operational fuel costs** by identifying and preventing **non-compliant refueling practices** across a logistics fleet.  
It also provides **insights into driver behavior**, **simulated cost savings** based on historical fuel patterns, and **story-driven visuals** that move beyond reporting to drive decision-making.
---

## 🧩 Methodology: DMAIC + CRISP-DM Hybrid

### 🟦 Define – Identify the Problem
Operations reported a growing cost discrepancy between planned and actual fuel expenditure.  
Upon investigation, it was discovered that several drivers were refueling at **unauthorized depots** where the **price per liter** was significantly higher than the company’s owned or preferred depots.  

- **Business impact:**  
  - Fuel price variance up to **$0.50 per liter**.  
  - Average fill volume per truck: ~800 liters.  
  - Potential excess cost per fill: **≈ $400**.  
  - With multiple fills per day across the fleet, this represented a **substantial avoidable expense**.

- **Goal:**  
  Develop a **Power BI dashboard** that identifies where and when unauthorized fuel fills occur, quantifies the financial impact, and enables operations to enforce depot allocation compliance.

---

### 🟨 Measure – Collect and Prepare the Data
Data sources were collected from multiple operational systems and standardized for analysis:
- **Fuel transactions:** Depot name, location, driver name, vehicle registration, fuel volume, price per liter, date/time.  
- **Trip data:** TripId, route, depot allocation, driver assignment.  
- **Operational unit data:** Region, depot ownership type, and target fuel rate.

Data preparation was completed in **Power Query**, where transformations included:
- Standardizing depot names and codes.  
- Merging transaction and trip tables on driver and date.  
- Creating calculated columns for authorized vs unauthorized depot fills.  
- Establishing KPIs for:
  - Fuel price variance per fill.  
  - Fuel cost per km.  
  - Total savings opportunity if compliant.

---

### 🟧 Analyze – Find the Root Cause
Using DAX measures and Power BI visuals, several analytical layers were created:

**1. Depot Cost Analysis**  
- Average fuel price per depot.  
- Comparison of owned vs non-owned depots.  
- Identification of high-cost depots used by unauthorized drivers.

**2. Driver Compliance Analysis**  
- % of fills at unauthorized depots per driver.  
- Total avoidable cost by driver and vehicle.  
- Trend over time to see if awareness or interventions reduced the issue.

**3. Regional/Operational Trends**  
- Map visual to identify depot hotspots.  
- Breakdown of cost variance per operational unit.

> 📊 Insight Example:  
> 18% of total fills occurred at unauthorized depots, resulting in an estimated monthly overspend of ~$23,000.

---

### 🟩 Improve – Implement and Track Corrective Actions
Based on the analysis, several operational interventions were implemented:
- Restricted fuel card access to **approved depots only**.  
- Introduced **driver training** and accountability measures.  
- Created a **weekly Power BI alert report** sent to fleet managers highlighting non-compliance.  
- Recommended **central depot refueling** planning for long-haul trips.

> 🧠 Operational outcome:  
> Within 2 months, unauthorized depot usage dropped by 72%, saving an estimated **R350,000+ per month**.

---

### 🟥 Control – Sustain the Improvement
To ensure ongoing control:
- The Power BI dashboard remains live and refreshes daily from the operational database.  
- Alerts and KPIs are monitored weekly by the control tower.  
- Continuous monitoring dashboards were built to highlight recurring patterns and identify any regressions.

> **Control KPIs:**
> - % of fills at unauthorized depots (target < 5%)  
> - Average fuel price per liter vs benchmark depot  
> - Monthly savings trend  

---

## 🛠 Tools and Techniques
- **Power BI Desktop** – Data modeling, visualization, KPI dashboards  
- **DAX** – Variance, scoring, and compliance metrics  
- **Power Query (M Language)** – Data transformation and merging  
- **Excel** – Initial validation and historical comparison  
- **DMAIC & CRISP-DM** – Framework for structured continuous improvement  

---

## 🧮 Sample DAX Measures

**1. Fuel Price Variance**
