# 🚦 Motor Vehicle Collision Analysis  

<img width="1080" height="1080" alt="Project Banner" src="https://github.com/user-attachments/assets/5f0d1d1b-ca5a-49ef-bf45-89621b1013ef" />

---

## 📌 Project Overview  
This project builds a **unified data architecture and warehouse** for traffic collision data from three major U.S. cities. By harmonizing disparate datasets, we enable scalable **business intelligence, visualization, and advanced analytics** around traffic safety.  

**Data Sources**  
- **Austin**: Crash Record Information System (CRIS) from TXDOT, populated by Texas Peace Officers and Austin PD  
- **Chicago**: CRIS crash database (10+ years), standardized with Austin schema  
- **NYC**: Motor Vehicle Collisions dataset (MV104-AN police reports), containing all police-reported accidents in NYC  

The final warehouse enables stakeholders to analyze:  
- 🚧 Accident hotspots  
- ⏰ Temporal trends (daily, seasonal, yearly)  
- 💥 Severity of incidents (injuries, fatalities)  
- 🚗 Contributing factors (driver behavior, weather, infrastructure)  

---

## 🗂️ Steps & Methodology  

### 🔍 Step 1: Understanding the Dataset  
- Explored schema, key fields, and relationships  
- Identified **data quality issues, nulls, and anomalies**  
- Designed a **unified schema** across all three cities  

### 📊 Step 2: Data Profiling with `ydata_profiling`  
- Imported datasets for initial assessment  
- Conducted **column profiling & transformation insights**  
- Reviewed data completeness and consistency  

### 🏗️ ETL & Data Processing  
- Built **ETL pipelines in Talend** for ingestion, cleaning, and transformation  
- Handled nulls, normalized categorical values, standardized vehicle types  
- Implemented **logging, pre-/post-job execution, and email notifications**  

### 🗃️ Dimensional Modeling  

<img width="1400" height="900" alt="image" src="https://github.com/user-attachments/assets/712f2a31-2650-4532-a4b8-66ae80fbb08c" />


**Dimensions**  
- `Dim_ContributingFactors` (SCD2 – tracks historical changes)  
- `Dim_VehicleType`  
- `Dim_Location`  
- `Dim_Date`, `Dim_Time`  

**Fact Tables**  
- `AccidentEventsFactTable` (injuries, fatalities, per road user type)  
- Bridge tables linking vehicles & contributing factors  

---

## 💡 Key Insights Enabled  
- 📈 **Accident Frequency** – citywide & comparative trends by day, week, month  
- 🗺️ **Hotspots** – geo-coordinates highlight high-risk intersections & streets  
- ⚠️ **Severity Analysis** – injuries & fatalities by city, vehicle, pedestrian/cyclist/motorist  
- 🕒 **Temporal Trends** – seasonal & hourly crash patterns  
- 🔎 **Contributing Factors** – distracted driving, speeding, weather & infrastructure  
- 🌆 **Comparative Analysis** – NYC vs Chicago vs Austin  

---

<img width="1500" height="1000" alt="image" src="https://github.com/user-attachments/assets/d40da649-fd18-4edd-8405-ea1c84cf567f" />


<img width="1400" height="1000" alt="image" src="https://github.com/user-attachments/assets/91696912-a370-46a6-af55-7c49e0f2a67f" />


## ⚙️ Tech Stack  

| Area                | Tools & Technologies                |
|---------------------|-------------------------------------|
| ETL / Integration   | Talend                              |
| Data Profiling      | Python, `ydata_profiling`           |
| Data Modeling       | Dimensional schema (Star Schema)    |
| Storage / Warehouse | SQL-based DW (DDL scripts included) |
| Visualization       | Tableau, Power BI (potential use)   |

---

## 🚀 Outcomes  
- ✅ Created a **scalable, unified traffic safety data warehouse**  
- ✅ Applied **ETL best practices**: logging, null handling, automation  
- ✅ Delivered a **blueprint for BI solutions in transportation analytics**  
- ✅ Enabled **insights into accident hotspots, severity patterns, and contributing causes**  

---

## 🏁 Conclusion  

This project unified crash data from **New York, Chicago, and Austin** into a reliable, scalable data warehouse.  
Through **data profiling, ETL pipelines in Talend, and dimensional modeling**, we built a system that ensures data quality, historical tracking (SCD2), and actionable insights.  

Key takeaways:  
- Ensured data integrity by carefully handling null values and inconsistencies  
- Designed a robust **star schema** with meaningful facts and dimensions  
- Captured evolving trends using **slowly changing dimensions (SCD2)**  
- Delivered insights on **accident hotspots, severity trends, and contributory factors**  

👉 Beyond insights into traffic safety, this project reinforced our expertise in **big data management, ETL best practices, and analytics-ready architectures** — serving as a **blueprint for future large-scale data solutions**.  

