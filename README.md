# 🏥 Health Care Analytics Dashboard

## 📌 Overview

The **Health Care Analytics Dashboard** provides an interactive, data-driven overview of hospital performance, patient demographics, doctor efficiency, billing distribution, and treatment costs.  
This project integrates **Excel**, **Python**, and **Power BI (with DAX)** to deliver deep insights into key healthcare metrics through dynamic and visually engaging dashboards.

---

## ⚙️ Tools & Technologies

| Tool | Purpose |
|------|----------|
| **Excel** | Data cleaning, transformation, and preprocessing |
| **Python (pandas, matplotlib, seaborn)** | Exploratory Data Analysis (EDA) and data validation |
| **Power BI** | Data modeling, visualization, and interactive dashboards |
| **DAX (Data Analysis Expressions)** | Custom measures, calculations, and dynamic titles |

---

## 📊 Dashboards Overview

### 1️⃣ Overview Dashboard

**Key Metrics (KPIs):**
- Total Billing Amount → £3M  
- Avg Billing Amount per Visit: £674.86  
- Total Medication Cost → £546K  
- Avg Medication Cost: £109.21  
- Total Treatment Cost → £3M  
- Avg Treatment Cost: £526.08  
- Total Insurance Coverage → £2M  
- Avg Insurance Coverage: £456.05  
- Out of Pocket → £1M  
- Avg Out of Pocket: £216.34  
- Total Room Charges → £180K  
- Avg Room Charges: £36.12  

**Visuals:**
- Column Chart: Total Billing Amount by Medical Procedure  
- Map Visual: Total Billing by States and Cities  
- Bar Chart: Total Billing Amount by Department  
- Line & Area Chart: Total of Visits and Avg Treatment Cost by Quarter  
- 100% Stacked Bar Chart: Total Billing Amount by Diagnosis and Service Type  

---

### 2️⃣ Patients Dashboard

**Key Metrics (KPIs):**
- Total Patients → 606  
- Avg Age: 49  
- Total Medication Cost → £67K  
- Avg Medication Cost: £110.85  
- Total Treatment Cost → £312K  
- Avg Treatment Cost: £514.88  
- Total Insurance Coverage → £272K  
- Avg Insurance Coverage: £448.99  
- Out of Pocket → £139K  
- Avg Out of Pocket: £229.92  
- Total Room Charges → £32K  
- Avg Room Charges: £53.18  

**Visuals:**
- Donut Charts: Total Visits by Insurance Provider / Gender / Service Type  
- Bar Charts: Patients by Age Group / Treatment Cost by Room Type / Visits by Department and Service Type  
- Information Panel: Appendicitis Overview (causes, symptoms, prevention)  
- Horizontal Bar Chart: Top Patients by Total Treatment Cost  

---

### 3️⃣ Doctors Dashboard

**Key Metrics (KPIs):**
- Total Outpatients → 2,511  
- Total Admitted Patients → 1,231  
- Average Doctor Rating → 4.21  
- Total Visits → 5,000  
- Non-Emergency Visits → 75.30%  
- Emergency Visits → 24.70%  

**Visuals:**
- Bar Chart: Patients by Length of Stay Group  
- Doctor Cards: Visual gallery of top doctors  
- Donut Charts: Emergency vs Non-Emergency Visits  
- Dynamic Line Chart: Visits by Month, Quarter, Weekdays, Year  
- Column Chart: Total Visits by Department and Service Group  

---

## 📈 Key DAX Measures

### 🔹 Totals
```DAX
Total Billing Amount = SUM(FactBilling[BillingAmount])
Total Medication Cost = SUM(FactBilling[MedicationCost])
Total Treatment Cost = SUM(FactBilling[TreatmentCost])
Total Insurance Coverage = SUM(FactBilling[InsuranceCoverage])
Total Out Of Pocket = SUM(FactBilling[OutOfPocket])
Total Room Charges = SUM(FactBilling[RoomCharges])
Total Patient = COUNTROWS(Patients)
Total Visits = COUNTROWS(Visits)
```

### 🔹 Averages
```DAX
Avg Billing Amount Per Visit = [Total Billing Amount] / [Total Visits]
Avg Medication Cost = [Total Medication Cost] / [Total Visits]
Avg Treatment Cost = [Total Treatment Cost] / [Total Visits]
Avg Insurance Coverage = [Total Insurance Coverage] / [Total Visits]
Avg Out Of Pocket = [Total Out Of Pocket] / [Total Visits]
Avg Room Charges = [Total Room Charges] / [Total Visits]
Avg Age = AVERAGE(Patients[Age])
```

### 🔹 Dynamic Title Example
```DAX
Dynamic Title =
SWITCH(
    SELECTEDVALUE('Dynamic Measures'[Dynamic Measures Order]),
    0, "Total Admission by Period",
    1, "Total Outpatient by Period",
    2, "Total Visits by Period"
)
```

---

## 🧩 Data Model Structure

**Fact Tables:**  
FactVisits, FactTreatment, FactPatients, FactDoctors  

**Dimension Tables:**  
Departments, insurance, Diagnoses, procedures, providers Cities (State, City, Flags), Date Table  

Relationships: One-to-Many between dimension and fact tables.

---

## 🎨 Dashboard Design

**Theme:** Dark modern healthcare interface  
**Color Palette:**  
- Light Blue `#A9D6F5`  
- Steel Blue `#7FB3D5`  
- Dark Gray `#1E1E1E`  

**Layout:** Rounded cards, soft shadows, and clear navigation buttons  
**Typography:** Bold metric cards with highlighted averages  

---

## 🚀 Project Workflow

1. **Data Preparation (Excel)** – Cleaned raw data, removed duplicates, handled missing values.  
2. **Exploratory Analysis (Python)** – Descriptive stats and EDA visualization using pandas and matplotlib.  
3. **Data Modeling (Power BI)** – Built star schema, defined relationships, created DAX measures.  
4. **Visualization & Interactivity** – Designed user-friendly dashboards with filters and slicers.  
5. **Dynamic Logic (DAX)** – Implemented switch measures and time-based analysis.

---

## 📁 Project Deliverables

| File | Description |
|------|--------------|
| `HealthCare_Overview.pbix` | Main Power BI dashboard file |
| `cleaned_health_data.xlsx` | Cleaned Excel dataset |
| `health_eda_report.py` | Python script for EDA |

---

## 🎯 Project Objectives

- Analyze and monitor hospital billing and treatment performance.  
- Understand patient demographics and visit trends.  
- Evaluate doctor performance and visit distribution.  
- Provide a unified, interactive view for healthcare decision-makers.

---

## 🔗 Author

**Mahmoud Mohamed Fawzy Elzayat**  
📍 *Data Analyst | Power BI | Python | Excel*  
🔗 [LinkedIn](https://www.linkedin.com/in/mahmoud-elzayat-data-analysis)  
🔗 [GitHub](https://github.com/M-Elzayat)
