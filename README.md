🏥 Health Care Analytics Dashboard
📌 Overview

The Health Care Analytics Dashboard provides an interactive, data-driven overview of hospital performance, patient demographics, doctor efficiency, billing distribution, and treatment costs.
This project integrates Excel, Python, and Power BI (with DAX) to deliver deep insights into key healthcare metrics through dynamic and visually engaging dashboards.

⚙️ Tools & Technologies
Tool	Purpose
Excel	Data cleaning, transformation, and preprocessing
Python (pandas, matplotlib, seaborn)	Exploratory Data Analysis (EDA) and data validation
Power BI	Data modeling, visualization, and interactive dashboards
DAX (Data Analysis Expressions)	Custom measures, calculations, and dynamic titles
📊 Dashboards Overview
1️⃣ Overview Dashboard

Key Metrics (KPIs):

Total Billing Amount → £3M
Avg Billing Amount per Visit: £674.86

Total Medication Cost → £546K
Avg Medication Cost: £109.21

Total Treatment Cost → £3M
Avg Treatment Cost: £526.08

Total Insurance Coverage → £2M
Avg Insurance Coverage: £456.05

Out of Pocket → £1M
Avg Out of Pocket: £216.34

Total Room Charges → £180K
Avg Room Charges: £36.12

Visuals:

Column Chart: Total Billing Amount by Medical Procedure
(X-Ray, CT Scan, MRI Scan, Ultrasound, Blood Test)

Map Visual: Total Billing by States and Cities

Bar Chart: Total Billing Amount by Department
(Cardiology, Orthopedics, General Surgery, Neurology, Pediatrics)

Line & Area Chart: Total of Visits and Avg Treatment Cost by Quarter
(Q1–Q4 with dynamic period selector)

100% Stacked Bar Chart: Total Billing Amount by Diagnosis and Service Type
(Hypertension, Appendicitis, Asthma, Fracture, Migraine)

2️⃣ Patients Dashboard

Key Metrics (KPIs):

Total Patients → 606
Avg Age: 49

Total Medication Cost → £67K
Avg Medication Cost: £110.85

Total Treatment Cost → £312K
Avg Treatment Cost: £514.88

Total Insurance Coverage → £272K
Avg Insurance Coverage: £448.99

Out of Pocket → £139K
Avg Out of Pocket: £229.92

Total Room Charges → £32K
Avg Room Charges: £53.18

Visuals:

Donut Charts:

Total Visits by Insurance Provider (AXA, Aviva, Allianz)

Total Patients by Gender (Male, Female)

Total Visits by Service Type (Outpatient, Emergency, Inpatient)

Bar Charts:

Total Patients by Age Group (Senior, Middle Age, Adult, Young Adult)

Total Treatment Cost by Room Type (Not Assigned, Private, Semi-Private, General)

Total Visits by Department and Service Type (Orthopedics, Pediatrics, General Surgery, Cardiology, Neurology)

Information Panel:

Appendicitis Overview — causes, symptoms, and prevention (visual + description)

Horizontal Bar Chart:

Top Patients by Total Treatment Cost
(Quinn Taylor, Fatima Balogun, Quinn Thompson, etc.)

3️⃣ Doctors Dashboard

Key Metrics (KPIs):

Total Outpatients → 2,511

Total Admitted Patients → 1,231

Average Doctor Rating → 4.21

Total Visits → 5,000

Non-Emergency Visits → 75.30%

Emergency Visits → 24.70%

Visuals:

Bar Chart: Total Patients by Length of Stay Group (1-Day, 2-4, 5-7, 8+)

Doctor Cards: Visual gallery of top doctors (with photos and names)

Donut Charts: Emergency vs Non-Emergency Visits

Dynamic Line Chart: Total Admission / Total Outpatient / Total Visits by Month, Quarter, Weekdays, Year
(Dynamic measure selection buttons)

Column Chart: Total Visits by Department and Service Group

Filter Pane: Filter by State (England, Northern Ireland, Scotland, Wales)

📈 Key DAX Measures

🔹 Totals Measures

Total Billing Amount = SUM(FactBilling[BillingAmount])
Total Medication Cost = SUM(FactBilling[MedicationCost])
Total Treatment Cost = SUM(FactBilling[TreatmentCost])
Total Insurance Coverage = SUM(FactBilling[InsuranceCoverage])
Total Out Of Pocket = SUM(FactBilling[OutOfPocket])
Total Room Charges = SUM(FactBilling[RoomCharges])
Total Patient = COUNTROWS(Patients)
Total Visits = COUNTROWS(Visits)

🔹 Average Measures

Avg Billing Amount Per Visit = [Total Billing Amount] / [Total Visits]
Avg Medication Cost = [Total Medication Cost] / [Total Visits]
Avg Treatment Cost = [Total Treatment Cost] / [Total Visits]
Avg Insurance Coverage = [Total Insurance Coverage] / [Total Visits]
Avg Out Of Pocket = [Total Out Of Pocket] / [Total Visits]
Avg Room Charges = [Total Room Charges] / [Total Visits]
Avg Age = AVERAGE(Patients[Age])

🔹 Dynamic Title Example

Dynamic Title =
SWITCH(
    SELECTEDVALUE('Dynamic Measures'[Dynamic Measures Order]),
    0, "Total Admission by Period",
    1, "Total Outpatient by Period",
    2, "Total Visits by Period"
)

🔹 Date Intelligence

Time filters based on Month, Quarter, Year, Weekdays, and WeekType

Dynamic date hierarchy used for trend analysis.

🧩 Data Model Structure

Fact Tables

FactBilling

FactVisits

FactTreatment

FactPatients

FactDoctors

Dimension Tables

Departments

Diagnoses

Cities (State, City, Flags)

insurance

procedures

providers

Date Table

Relationships: One-to-Many between dimension tables and fact tables.

🎨 Dashboard Design

Theme: Dark modern healthcare interface

Color Palette:

Light Blue #A9D6F5

Steel Blue #7FB3D5

Dark Gray Background #1E1E1E

Layout: Rounded card containers, soft shadows, and minimal contrast

Navigation Buttons: Overview | Patients | Doctors | Filters

Typography: Bold metric cards with highlighted averages

🚀 Project Workflow

Data Preparation (Excel)

Cleaned raw hospital data, removed duplicates, handled missing values.

Exploratory Analysis (Python)

Used pandas for descriptive stats and matplotlib/seaborn for EDA visualization.

Data Modeling (Power BI)

Built star schema, defined relationships, created DAX measures.

Visualization & Interactivity

Designed user-friendly dashboards with filters, slicers, and navigation tabs.

Dynamic Logic (DAX)

Implemented switch measures, dynamic titles, and time-based analysis.

📁 Project Deliverables
File	Description
HealthCare_Overview.pbix	Main Power BI dashboard file
cleaned_health_data.xlsx	Cleaned Excel data used for analysis
health_eda_report.py	Python script for exploratory analysis
🎯 Project Objectives

Analyze and monitor hospital billing and treatment performance.

Understand patient demographics and visit trends.

Evaluate doctor performance and visit distribution.

Provide a unified, interactive view for healthcare decision-makers.

🔗 Author

Mahmoud Mohamed Fawzy Elzayat
📍 Data Analyst | Power BI | Python | Excel
🔗 LinkedIn
🔗 GitHub
