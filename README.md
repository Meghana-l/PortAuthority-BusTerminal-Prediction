# 🚍 Port Authority Bus Terminal Passenger Prediction (2025–2030)

![Power BI](https://img.shields.io/badge/Power%20BI-FFB900?style=for-the-badge&logo=power-bi&logoColor=white)
![R](https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-336791?style=for-the-badge&logo=postgresql&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Excel](https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)



### 📊 University of New Haven – Pompea College of Business  
**Course:** BANL-6430-03 – Database Management for Business Analytics  
**Instructor:** Dr. Pindaro Demertzoglou  
**Team Members:**  
- Meghana Lakshminarayana Swamy  
- Aastha Kale  
- Ayesha Kabir  
- Rajyalakshmi Nelakurthi  
- Venkata Sai Phanindra Namburu  

---

## 🧠 Project Overview

This project, *Port Authority Bus Terminal Passenger Prediction*, was created to provide the **Port Authority of New York** with actionable insights to improve **bus terminal operations, maintenance planning, and passenger forecasting** for 2025–2030.

It combines **SQL data integration**, **R-based modeling**, and **Power BI visualization** into a cohesive analytical solution.

---

## 🎯 Business Objectives

1. Forecast passenger traffic from 2025–2030.  
2. Identify key factors affecting mechanical reliability.  
3. Evaluate carrier-level performance and distribution.  
4. Determine the busiest travel periods.  
5. Classify boroughs based on operational reliability.

---

## 🧩 Data Sources

Data was gathered, cleaned, and integrated from three main sources:

| Source | Description |
|--------|-------------|
| **MTA Bus Mechanical Failure Data** | Monthly failures, mileage, and reliability metrics. |
| **Weather Dataset (Tbl_Weather)** | Daily temperature, precipitation, and snowfall data aggregated by month. |
| **Traffic Data** | Daily vehicle traffic counts per borough. |

Data preprocessing and joins were performed in **SQL Server Management Studio (SSMS)**. Missing weather data was handled via mean-based imputation and aggregated at monthly level.

---

## 🧮 Analytical Models

| Model | Purpose | Key Findings |
|--------|----------|--------------|
| **Multiple Linear Regression** | Predict Mean Distance Between Failures (MDBF) | Explained 71.2% variance; `Monthly_Miles` (+), `Road_Call_Count` (–) significant. |
| **Logistic Regression** | Classify high vs. low failure months | Accuracy: 63.8%; higher mileage correlated with fewer breakdowns. |
| **K-Means Clustering** | Group boroughs by failure and reliability | 3 clusters found: *High Failure Urban Core*, *Moderate Risk High Activity*, *Low Risk Zone*. |
| **Time Series Forecasting** | Forecast passenger traffic 2025–2030 | Seasonal trend stable; peaks in summer, dips in winter. |
| **Random Forest** | Identify strongest predictors | `Road_Call_Count` contributed ~80% importance for MDBF prediction. |

---

## 💻 Tools & Technologies

| Category | Tools Used |
|-----------|-------------|
| Data Management | SQL Server, Excel |
| Modeling & Analysis | R (tidyverse, caret, factoextra), Python (Pandas, Scikit-learn) |
| Visualization | Power BI |
| Collaboration | GitHub |

---

## 📊 Power BI Dashboard

The interactive Power BI dashboard consists of **five key pages**, each answering one business question.

---

### 🖼️ 1. Passenger Forecast (2025–2030)

**What it shows:**  
A time-series forecast predicting passenger volume for 2025–2030 using 2013 monthly data. It visualizes expected seasonal fluctuations, helping forecast resource demand.

**Key takeaway:**  
Traffic trends remain stable with summer peaks and winter dips.

<img width="1312" height="718" alt="Screenshot 2025-10-22 220647" src="https://github.com/user-attachments/assets/f9563a3c-3472-49e4-b988-fbaae627a433" />

---

### 🖼️ 2. Key Predictive Factors for Passenger Volume

**What it shows:**  
A Random Forest model visualization ranking variable importance (e.g., Monthly Road Calls, Mileage, Temperature) and displaying how mechanical and weather factors affect passenger flow.

**Key takeaway:**  
Road Calls and Mileage are the strongest predictors of operational reliability.

<img width="1314" height="739" alt="Screenshot 2025-10-22 220835" src="https://github.com/user-attachments/assets/ed9ed03f-ad8d-4479-abcf-6ed79f98bee7" />

---

### 🖼️ 3. Carrier-Wise Passenger Projection

**What it shows:**  
Visualizes passenger traffic by carriers such as MTA and NJ Transit using bar and donut charts. Helps identify which carriers handle the largest load and where capacity upgrades may be needed.

**Key takeaway:**  
Certain carriers consistently serve higher passenger volumes — critical for planning resource allocation.

<img width="1312" height="740" alt="Screenshot 2025-10-22 221038" src="https://github.com/user-attachments/assets/29b856e4-45f6-4740-a9d6-74276d5bb2db" />

---

### 🖼️ 4. Busiest Time Periods (Week, Month, Year)

**What it shows:**  
Displays patterns across weekdays, months, and years to pinpoint high-demand periods using line and column charts.

**Key takeaway:**  
- July and October emerge as peak months.  
- Consistent weekday ridership with small Sunday dips.


<img width="1321" height="747" alt="Screenshot 2025-10-22 221427" src="https://github.com/user-attachments/assets/7c4154e1-4f0e-440f-9aeb-c61741a1bf25" />

---

### 🖼️ 5. Borough Risk Classification (Clustering)

**What it shows:**  
Boroughs grouped using K-Means clustering based on MDBF, breakdown counts, and weather factors.  
Each cluster is color-coded to indicate operational risk.

**Key takeaway:**  
- **High Risk:** Bronx & Manhattan  
- **Moderate:** Brooklyn & Queens  
- **Low Risk:** Staten Island

<img width="1311" height="753" alt="Screenshot 2025-10-22 221609" src="https://github.com/user-attachments/assets/80b7e601-79ce-4619-ba6e-923993d609d3" />

---

## 🔍 Insights Summary

- **Mechanical strain**, not weather, drives most reliability issues.  
- **Bronx and Manhattan** face the highest failure rates.  
- **Staten Island** demonstrates best reliability (highest MDBF).  
- Predictive maintenance should focus on high-risk boroughs.  
- Missing post-2016 data limits long-term forecasting accuracy.

---

## 💡 Recommendations

1. Collect and integrate **real passenger counts** for stronger forecasting.  
2. Incorporate **event-based factors** (holidays, strikes, concerts).  
3. Establish **IoT-based vehicle tracking** for predictive maintenance.  
4. Update datasets to include **2017–2024** for better model accuracy.  
5. Automate dashboard refresh using **Power BI Service**.

---

## 🧑‍🤝‍🧑 Team Contributions

**Meghana Lakshminarayana Swamy & Aastha Kale**  
- Built Power BI dashboard and SQL data pipeline.  
- Led report writing and regression/classification modeling.  

**Rajyalakshmi Nelakurthi**  
- Designed and structured final presentation visuals.  

**Venkata Sai Phanindra Namburu**  
- Scripted the final presentation and summarized insights.  

**Ayesha Kabir**  
- Validated data quality and assisted in dashboard testing.

---

## 🏁 Conclusion

This project demonstrates how **data engineering, predictive analytics, and visualization** can improve **transportation operations**.  
The insights provide a foundation for **strategic maintenance**, **capacity planning**, and **passenger forecasting** at the Port Authority Bus Terminal.

---

## 🧾 License

This work is part of the BANL-6430 course at the University of New Haven and is intended for academic and portfolio use only.
