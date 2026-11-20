# 🏥 Hospital System Analysis | Power BI Dashboard

An interactive Power BI dashboard that analyzes a hospital's **appointments, billing, treatments, doctors, and patients** for 2023, to track revenue, payment collection, appointment attendance, and doctor workload.
---

## 🎯 Objective

Give hospital management a clear view of:

- How much revenue is generated, and how much of it is actually collected?
- How does revenue change from month to month?
- How many appointments are completed vs. cancelled or missed (no-shows)?
- How is the workload distributed across doctors, specializations, and visit reasons?
- Who are the patients and what insurance providers do they use?

---

## 🛠️ Tools & Skills

| Area | Details |
|---|---|
| **BI Tool** | Power BI Desktop |
| **Data Modeling** | Star schema: fact tables (`Fact Bill`, `Fact Appointment`, `Fact Treatment`) connected to dimension tables (`Dim Doctors`, `Dim Patients`, `DimDate`) |
| **DAX** | Total Revenue, Month-over-Month revenue and %, previous-month revenue, appointment counts, average revenue per appointment, average treatment cost, distinct counts |
| **Data Preparation** | Power Query |
| **Visualization** | KPI cards, donut charts, bar/column charts, line chart, tables, slicers, cover page with navigation buttons |

---

## 📂 Dataset

5 CSV files (in the `data/` folder). Period: **January – December 2023**.

| File | Rows | Description |
|---|---|---|
| `appointments.csv` | 200 | Appointment date/time, reason for visit, status |
| `billing.csv` | 200 | Bill amount, payment method, payment status |
| `treatments.csv` | 200 | Treatment type, description, cost |
| `doctors.csv` | 10 | Specialization, experience, hospital branch |
| `patients.csv` | 50 | Gender, date of birth, insurance provider |

> **Note:** This is a sample/practice dataset, not real hospital data.

---

## 📊 Dashboard Pages

### 1. Cover Page
Title page with navigation buttons to the other pages.

### 2. Billing
- KPI cards: **Total Revenue**, **Revenue MoM**, **Revenue MoM %**, **Last Month Revenue**
- Revenue by payment method and by payment status (donut charts)
- Top 10 patients and top 10 treatments by revenue
- Slicers: Month, Payment Method

### 3. Appointments
- KPI cards: **Number of Appointments**, **Average Revenue per Appointment**
- Appointments by status, by month, by doctor, by patient, and by reason of visit
- Slicers: Doctor, Month, Status

### 4. Doctors & Treatments
- KPI cards: **Total Doctors**, **Total Patients**, **Total Treatments**, **Average Treatment Cost**
- Doctors by specialization, patients by gender, patients by insurance provider
- Top 10 appointments by treatment cost

---

## 🧮 DAX Measures

Total Revenue · Revenue Last Month · Revenue MOM · Revenue MOM % · Number of Appointment · Average Revenue per Appointment · Average Treatment Cost · Total Doctors · Total Patients · Total Treatments

---

## 💡 Key Insights

1. **Collection problem:** Of **$551K** billed in 2023, only about **31% ($173K) was paid**. Around **35% ($193K) failed** and **33% ($185K) is still pending**.
2. **Low attendance:** Only **23%** of appointments were completed. **26% were no-shows** and **25.5% were cancelled**. Consultations had the lowest completion rate (about 9%) and the highest cancellation rate (35%).
3. **Volatile revenue:** Monthly revenue ranged from **$64.3K in April** to **$27.6K in December** (a **47.5% drop** month over month), so revenue forecasting needs care.
4. **Workload is concentrated:** Pediatrics accounts for **49%** of appointments, followed by Dermatology (35%) and Oncology (16%). The busiest doctor handled 29 appointments vs. 13 for the least busy.
5. **Revenue is concentrated in a few patients:** The top 10 patients (20% of all patients) generate about **37%** of total revenue.
6. **Highest-cost treatment:** MRI has the highest average cost (about **$3,225**), compared to about $2,500–$2,800 for the other treatments.

---

## 📁 Repository Structure

```
hospital-system-analysis/
├── README.md
├── hospital_Dashboard.pbix
│── appointments.csv
├── billing.csv
├── doctors.csv
├── patients.csv
└── treatments.csv
├── cover-page.png
├── billing-page.png
├── appointments-page.png
└── doctors-treatments-page.png
```

## ▶️ How to Use

1. Download `hospital_Dashboard.pbix`.
2. Open it with **Power BI Desktop** (free).
3. If prompted, update the data source path to the CSV files in the `data/` folder.

---

## 👤 Author

**Muhammed Mokhtar** — Data Analyst
📍 Alexandria, Egypt
🔗 [LinkedIn](https://linkedin.com/in/mohammed-mokhtar-3126a1167)
