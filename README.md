# PowerBi-Hospital-Transaction-Project

# 🏥 Hospital Transaction Dashboard – Power BI Project

![Dashboard Overview](https://github.com/DamiOlanre1976/PowerBi-Hospital-Transaction-Project/blob/main/Hospital%20Transaction%20Dashboard%202.JPG)

## 📘 Project Summary

This Power BI project presents a comprehensive **Hospital Transaction Dashboard** built using a star schema data model and DAX measures. It enables decision-makers to monitor key performance indicators like revenue, profit, patient volume, and doctor performance, and make data-driven decisions for operational efficiency and growth.

---

## 📌 Objectives

- Analyze hospital financial metrics (revenue, expenses, profit).
- Track patient and doctor activity over time.
- Identify top-performing doctors and high-value patients.
- Explore trends and specialty-wise distributions.
- Offer actionable insights and strategic recommendations.

---

## 🧩 Data Model (Star Schema)

The data model is structured using a star schema centered around a transactional fact table and linked dimension tables.

![Data Model Screenshot](https://github.com/DamiOlanre1976/PowerBi-Hospital-Transaction-Project/blob/main/Hospital%20Transaction%20Star%20Schema%20-%20Data%20Modeling.JPG)

### 📁 Fact Table – `Hospital_Fact`

| Column           | Description                        |
|------------------|------------------------------------|
| Date             | Date of transaction                |
| DoctorID         | Foreign key to `Doctor_Dim`        |
| PatientID        | Foreign key to `Patient_Dim`       |
| LocationID       | Foreign key to `Location_Dim`      |
| ProcedureID      | Foreign key to `Procedure_Dim`     |
| RevenueAmount    | Total revenue for the transaction  |
| ExpenseAmount    | Associated cost                    |
| TransactionID    | Unique identifier                  |

### 📁 Dimension Tables

- **Doctor_Dim** – Doctor ID, name, gender, specialty, contact info
- **Patient_Dim** – Patient ID, name, gender, DOB, address
- **Procedure_Dim** – Procedure ID, name, category, description
- **Location_Dim** – Location ID, city, state, postal code
- **Calendar Table** – Date hierarchy with day, month, quarter, and year

---
## 🧮 DAX Measures

```dax
-- Financial Metrics
Total Revenue = SUM(Hospital_Fact[RevenueAmount])
Total Expenses = SUM(Hospital_Fact[ExpenseAmount])
Total Profit = [Total Revenue] - [Total Expenses]
Profit Margin = DIVIDE([Total Profit], [Total Revenue], 0)

-- Doctor & Patient Counts
No of Doctors = DISTINCTCOUNT(Doctor_Dim[DoctorID])
No of Patients = DISTINCTCOUNT(Patient_Dim[PatientID])

---
# 📊 Key Insights & Recommendations

This project summarizes the **key business insights** derived from the Power BI hospital transaction dashboard, along with **strategic recommendations** to support decision-making in hospital operations, staffing, and patient services.

---

## 🔍 Key Insights

### 1. Top Revenue Contributors
- **Dr. Ava Adams** generated the highest revenue: **\$25,000**.
- Other top-performing doctors include **Liam Turner** and **Benjamin Lane**.
- **Harper Young** and **Ethan Lopez** were the **top patients** in terms of revenue contribution, each accounting for over **\$15,000**.

### 2. Patient Volume Trends
- Patient count **peaked in Q4 2021** (32 patients).
- A **significant decline** in patient visits is evident in **2023**, particularly in Q2 and Q3 (dropping to 8–12 patients per quarter).

### 3. Gender Representation
- Doctors: 42 Male / 39 Female  
- Patients: 39 Male / 47 Female  
- The hospital maintains a **balanced gender distribution** among both patients and healthcare providers.

### 4. Specialty Utilization
- **Cardiology**, **Dermatology**, and **Neurology** had the **highest engagement** in terms of both doctor and patient activity.
- **Orthopedic** and **Ophthalmology** specialties are **underutilized**, with relatively low doctor and patient participation.

---

## 💡 Strategic Recommendations

### 1. Promote High-Performing Doctors & Procedures
- Identify and replicate the best practices used by **top-earning doctors**.
- Feature high-performing procedures in promotional materials or patient education campaigns.

### 2. Investigate the Decline in Patient Numbers (2023)
- Conduct a thorough review to understand the cause:
  - Is it due to reduced staffing?
  - External events like health policy changes?
  - Lower patient satisfaction?
- Run surveys or focus groups to gather patient feedback.

### 3. Boost Underutilized Specialties
- Reassess service delivery and marketing for **Orthopedics** and **Ophthalmology**.
- Consider hiring more specialists or redistributing patient flow through referrals.
- Offer public awareness sessions about the importance of these services.

### 4. Improve Patient Retention
- Develop a **follow-up program** or loyalty plan for high-value patients.
- Use reminders for appointments and check-ups to increase return rates.
- Monitor first-time vs. repeat patient behavior.

### 5. Resource Planning Based on Trends
- Align **doctor schedules and staff allocation** with quarterly trends (e.g., Q4 peak).
- Prepare for increased demand during busier periods using past data.
- Use Power BI alerts and data-driven workflows to notify managers during spikes.

---

## ✅ Conclusion

These insights and recommendations aim to improve hospital operations, financial outcomes, and patient experience. By aligning strategic decisions with data, hospitals can better allocate resources, enhance patient satisfaction, and maximize healthcare outcomes.

---
 
🧠 **Full Dashboard**: See the main repository for visuals and data model


## 👨‍💻 Author

**[Damilola Lasode]**  
📧 [damilolalasode10@gmail.com]  
🌐 GitHub: [https://github.com/DamiOlanre1976](https://github.com/DamiOlanre1976)

