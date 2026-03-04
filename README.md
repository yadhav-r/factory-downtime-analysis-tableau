# Factory Machine Downtime Analysis (Tableau)

## Project Overview

This project analyzes machine telemetry data from multiple Daikibo factories to identify patterns of machine downtime. The goal of the analysis is to determine which factories and machine types contribute most to operational downtime, enabling better maintenance planning and operational efficiency.

The analysis was performed using **Tableau**, where telemetry data was transformed into an interactive dashboard for easier exploration and decision-making.

---

## Problem Statement

Manufacturing plants often experience machine downtime due to equipment health issues. Identifying the machines and locations responsible for the highest downtime is essential for improving productivity and minimizing operational losses.

This project aims to answer the following questions:

* Which factory experiences the highest machine downtime?
* Which machine types contribute most to downtime?
* How does machine health status impact overall factory performance?

---

## Dataset

The dataset used in this project is the **Daikibo Telemetry Dataset**, which contains machine health data collected across multiple factories.

### Key Data Fields

| Field        | Description                                 |
| ------------ | ------------------------------------------- |
| Factory      | Factory location                            |
| Machine Type | Type of machine used in production          |
| Status       | Machine health status (healthy / unhealthy) |

### Factories Included

* Berlin (Germany)
* Meiyo (Tokyo, Japan)
* Seiko (Osaka, Japan)
* Shenzhen (China)

---

## Tools & Technologies

The following tools were used for the analysis:

* **Tableau** – Data visualization and dashboard development
* **Calculated Fields** – Data transformation and metric creation
* **Interactive Dashboards** – Visual analysis of machine performance

---

## Data Preparation

A calculated field called **Unhealthy Downtime** was created in Tableau to estimate downtime.

### Calculated Field Logic

```
IF [status] = "unhealthy" THEN 10 ELSE 0 END
```

Each record marked as **unhealthy** represents **10 minutes of machine downtime**.

This transformation allowed downtime to be aggregated and analyzed across factories and machine types.

---

## Dashboard Features

The Tableau dashboard provides several analytical views:

* Factory-wise downtime comparison
* Machine type downtime distribution
* Identification of machines causing the highest downtime
* Interactive filtering for better exploration

The visualization allows quick identification of operational inefficiencies.

---

## Key Insights

### Highest Downtime Factory

**Seiko (Osaka)** recorded the highest machine downtime among all factories.

### Machine Causing Maximum Downtime

The **LaserWelder** machine type was responsible for the highest downtime across the dataset.

### Operational Observation

Downtime is unevenly distributed across factories and machine types, suggesting that targeted maintenance strategies could significantly reduce productivity loss.

---

## Dashboard Preview

The interactive Tableau dashboard visualizes machine downtime across factories and machine types.

![Dashboard](dashboard.png)

---

## Future Improvements

Potential enhancements for this project include:

* Integrating real-time telemetry data
* Adding predictive maintenance models
* Extending the analysis using Python or SQL
* Creating additional KPI-based dashboards

---

## Author

**Yadhav R**
BTech Student | Aspiring Data Analyst
Interested in Data Analytics, Machine Learning, and AI Systems
