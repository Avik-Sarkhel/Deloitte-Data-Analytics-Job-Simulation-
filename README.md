[![GitHub Repo](https://img.shields.io/badge/GitHub-View%20Repository-181717?logo=github)](https://github.com/Avik-Sarkhel/Deloitte-Data-Analytics-Job-Simulation-)

# 💼 Deloitte Job Simulation (Forage) Project

This repository contains the deliverables for the **Deloitte Data Analytics Virtual Internship** hosted on **Forage**, completed during **June–July**. The project is divided into two tasks focused on real-world data processing, visualization, and classification using **Power BI** and **Excel**.

---

## 📊 Project Overview

Through this simulation, I:
- Explored how Deloitte analysts approach data problems
- Built interactive dashboards to analyze machine telemetry
- Classified compensation equality using formula-driven Excel logic
- Enhanced insights with color coding, branding, and clean design

---

## ✅ Tasks Completed

---

### 📌 Task 1: Telemetry Data Analysis & Dashboard Creation (Power BI)

#### 🎯 Objective
Analyze telemetry data from **Daikibo's 4 factories** to answer:
1. **Which factory had the most machine failures?**
2. **Which machines failed most frequently in that factory?**

#### 🧠 Background
- Factories: **Meiyo**, **Seiko**, **Berlin**, **Shenzhen**
- Each with **9 machine types**, sending messages every **10 minutes**
- One month of data → **May 2021**
- File: `daikibo-telemetry-data.json`

#### 🧰 Power BI Process

- **Data Import**:
  - Imported JSON → expanded all nested columns (e.g., `location`, `data`)
  - Result: **160,704 rows**, **10 columns**

- **Data Transformation**:
  - Created new calculated column: `Unhealthy`  
    - `10` if `status = "unhealthy"` (represents 10 minutes of downtime)
  - Cleaned data types for accurate analysis

- **Dashboard Creation**:
  - Chart 1: **Down Time per Factory**
  - Chart 2: **Down Time per Device Type**
  - Combined in a dashboard → set **factory chart as filter** for device chart

#### 📸 Visual Outputs

##### 🖼️ Dashboard Screenshot
![Task 1 Dashboard](./Task%201%20Given%20Solution.png)

##### 🎞️ Dashboard Recording
![Dashboard Recording](./Dashboard%20Recording%20(1).gif)

#### 📁 Task 1 Files
- `Deloitte Job Simulation Task 1.pbix`
- `Task 1 Given Solution.png`
- `Dashboard Recording (1).gif`

---

### 📌 Task 2: Compensation Equality Classification (Excel)

#### 🎯 Objective
Assess employee compensation fairness using equality scores.

#### 📝 Input Columns:
- `Factory`
- `Job Role`
- `Equality Score` (from -100 to +100)

#### 🧪 Classification Logic

| Equality Score Range | Equality Class           |
|----------------------|--------------------------|
| **Between -10 and 10** (inclusive) | Fair |
| **Between -20 to -11 OR 11 to 20** | Unfair |
| **Less than -20 OR greater than 20** | Highly Discriminative |

#### 🧮 Excel Formula Used
excel
=IF(ABS(C2)<=10, "Fair", IF(ABS(C2)<=20, "Unfair", "Highly Discriminative"))

✅ ABS() ensures classification is based on the absolute distance from perfect equality (0). This helps simplify logic — for example: both -9 and +9 are considered equally fair.

#### 🧠 Note on "Fair" Classification:
The formula classifies a score as Fair if it falls within -10 to +10 (inclusive). This captures minor deviations from equality and considers them acceptable in most organizational contexts.

#### 🎨 Visual Enhancements
✅ Conditional Formatting applied to the Equality class column:

🔴 Red → Highly Discriminative

🟡 Yellow → Unfair

🟢 Green → Fair

#### ✅ Excel table was styled to match Deloitte’s brand theme:

Structured table format

Professional borders, headers, and filtered columns

#### 📸 Visual Outputs
### 📸 Visual Outputs

##### 🖼️ Original Excel File (As Provided)
![Original Excel File](./TASK%202%20EXCEL.png)

##### 🖼️ My Classified & Styled Excel Output
![My Solution](./TASK%202%20MY%20SOLUTION.png)

##### 🖼️ Deloitte’s Provided Solution (Reference)
![Deloitte Solution](./TASK%202%20GIVEN%20SOLUTION.png)

#### 📁 Task 2 Deliverables
📄 Job Simulation Task 2.xlsx — Final processed Excel file

📄 Task 5 Equality Table (1).xlsx — Raw or intermediate file

🖼️ TASK 2 EXCEL.png — Screenshot of the original Excel structure

🖼️ TASK 2 MY SOLUTION.png — My classified and styled version

🖼️ TASK 2 GIVEN SOLUTION.png — Deloitte's sample solution

📄 Task 5 Model Answer.xlsx — (If provided)
