# HVMV Power Supply Capacity & Target Commission Pipeline Analytics

## 📌 1. Project Overview
This enterprise Data Analytics & Power BI project tracks and analyzes the **High Voltage (HV)** and **Medium Voltage (MV)** power supply request pipeline across multiple industry sectors in Malaysia. 

The dataset contains **227 projects**[cite: 5] representing a total Maximum Demand (MD) of **~18,191 MW**[cite: 5]. The analysis monitors project progression across 8 key stages (from *Pre-Consultation* to *Completed*)[cite: 5], calculates completed vs. balance capacities[cite: 5], and projects target commission structures based on qualification stages[cite: 5].

---

## 🛠️ 2. Tech Stack & Data Modeling
* **Business Intelligence:** Power BI (DAX Measures, Custom Visuals, Interactive Slicers)
* **Data Transformation & Prep:** Power Query / Excel (Data Cleaning, Schema Standardization, Custom ID Mappings)
* **Data Schema:** Star Schema linking Fact Table (`Project Details`)[cite: 5] with Dimension Tables (`Sector_List`, `Stage_List`, `Commission Target`)[cite: 5].

---

## 📊 3. Key Findings & Pipeline Summary

### 1. Overall Capacity & Project Status
* **Total Projects Tracked:** 227 projects[cite: 5]
* **Total Maximum Demand (MD):** 18,190.75 MW[cite: 5]
* **Completed Capacity:** 1,410.54 MW (74 projects completed)[cite: 5]
* **In-Progress Pipeline (Balance Capacity):** 16,780.20 MW (153 projects in progress)[cite: 5]

### 2. Voltage Breakdown
* **High Voltage (HV):** 96 projects[cite: 5] accounting for **15,995.18 MW** (~88% of total demand)[cite: 5], heavily driven by Data Center requests[cite: 5].
* **Medium Voltage (MV):** 131 projects[cite: 5] accounting for **679.95 MW**[cite: 5], predominantly across Logistics, Manufacturing, and Federal Government sectors[cite: 5].

### 3. Sector Distribution
* **Data Centers:** The largest growth driver with **63 projects** totaling **12,392.16 MW**[cite: 5].
* **Manufacturing:** 33 projects totaling **2,727.35 MW**[cite: 5].
* **Logistics & Transportation:** 57 projects totaling **978.66 MW**[cite: 5].
* **Federal Government:** 70 projects totaling **230.68 MW**[cite: 5].
* **Real Estate & Healthcare:** 3 projects totaling **318.18 MW**[cite: 5].

---

## 💰 4. Target Commission Qualification Logic

The model incorporates stage-based target commission qualification rules[cite: 5]:
* **Pre-Consult / Prospect Stage:** 0% (Not eligible)[cite: 5]
* **Official Supply Submission:** Qualified at **0.10% × MD (MW)**[cite: 5]
* **CPP Approval:** Qualified at **0.20% × MD (MW)**[cite: 5]
* **Technical & Commercial Approval:** Qualified at **0.30% × MD (MW)**[cite: 5]

---

## 🚀 5. Dashboard Preview & Visualizations

### Executive Pipeline Overview
![Executive Overview](./assets/executive_summary.png)

### Sector & Voltage Breakdown
![Sector Breakdown](./assets/sector_breakdown.png)

---

## 📁 6. Repository Structure
```text
├── data/
│   └── dataset_hvmv_report_New.xlsx    # Source Excel Dataset
├── pbix/
│   └── HVMV_Pipeline_Dashboard.pbix    # Interactive Power BI File
├── assets/
│   └── executive_summary.png           # Visual Screenshots
└── README.md                           # Documentation
