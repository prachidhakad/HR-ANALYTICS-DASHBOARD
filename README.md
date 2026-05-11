# HR Analytics Dashboard — Employee Attrition Analysis

> An interactive Power BI dashboard that identifies **why employees are leaving** by analyzing attrition patterns across demographics, salary, job roles, and tenure.



---


## 🔍 Overview
Employee attrition is one of the most costly challenges faced by modern organizations. This project presents an **interactive HR Analytics Dashboard** built in Power BI to help HR professionals and management understand:

- **Who** is leaving
- **Why** they are leaving
- **When** they tend to leave

The dashboard analyzes a real-world HR dataset of **1,470 employees** with an overall attrition rate of **16.1% (237 employees)**. It delivers actionable visual insights across six dimensions — age, education, salary, job role, years at company, and marital status — with department-level filtering across **Human Resources**, **Research & Development**, and **Sales**.

---

## ❗ Problem Statement

Organizations spend significant resources recruiting, onboarding, and training employees. When employees leave unexpectedly, it results in:

-  High recruitment and retraining costs
- Loss of institutional knowledge and team continuity
- Reduced morale among remaining employees
-  Disrupted project timelines and productivity

> **Core question this dashboard answers:**
> *"What are the key factors driving employee attrition, and which employee segments are most at risk of leaving?"*

By identifying high-risk groups early, HR teams can take proactive steps — such as salary reviews, targeted engagement programs, or improved onboarding — to reduce attrition before it happens.

---

## 🗂️ Dataset

| Property | Details |
|---|---|
| **Source** | IBM HR Analytics Employee Attrition & Performance |
| **Format** | Microsoft Excel (.xlsx) |
| **Total Records** | 1,470 employees |
| **Total Columns** | 38 |

<details>
<summary><strong>📋 Column Reference (click to expand)</strong></summary>

| Column | Description |
|---|---|
| `EmpID` | Unique employee identifier |
| `Age` | Employee age |
| `AgeGroup` | Categorized age bracket (18–25, 26–35, 36–45, 46–55, 55+) |
| `Attrition` | Whether the employee left — Yes / No |
| `BusinessTravel` | Frequency of business travel |
| `DailyRate` | Daily compensation rate |
| `Department` | Department — HR, Research & Development, Sales |
| `DistanceFromHome` | Commute distance in km/miles |
| `Education` | Education level on a 1–5 scale |
| `EducationField` | Field of educational background |
| `EmployeeCount` | Always 1 (per-record indicator) |
| `EmployeeNumber` | Internal employee number |
| `EnvironmentSatisfaction` | Work environment satisfaction rating (1–4) |
| `Gender` | Employee gender |
| `HourlyRate` | Hourly compensation rate |
| `JobInvolvement` | Level of job involvement (1–4) |
| `JobLevel` | Seniority level (1–5) |
| `JobRole` | Specific job title/role |
| `JobSatisfaction` | Job satisfaction rating (1–4) |
| `MaritalStatus` | Marital status — Single / Married / Divorced |
| `MonthlyIncome` | Monthly salary in USD |
| `SalarySlab` | Salary category — Upto 5k / 5k–10k / 10k–15k / 15k+ |
| `MonthlyRate` | Monthly rate |
| `NumCompaniesWorked` | Number of previous employers |
| `Over18` | Whether employee is over 18 |
| `OverTime` | Whether employee works overtime — Yes / No |
| `PercentSalaryHike` | Last salary hike percentage |
| `PerformanceRating` | Performance rating (1–4) |
| `RelationshipSatisfaction` | Satisfaction with work relationships (1–4) |
| `StandardHours` | Standard working hours (always 80) |
| `StockOptionLevel` | Stock option grant level (0–3) |
| `TotalWorkingYears` | Total years of professional experience |
| `TrainingTimesLastYear` | Number of training sessions attended last year |
| `WorkLifeBalance` | Work-life balance rating (1–4) |
| `YearsAtCompany` | Number of years at the current company |
| `YearsInCurrentRole` | Years spent in the current job role |
| `YearsSinceLastPromotion` | Years elapsed since last promotion |
| `YearsWithCurrManager` | Years working under current manager |

</details>

---

## 💡 Key Insights

- **Year 1 is the highest-risk period** — 59 employees left within their first year, making early tenure the single most critical attrition window. 
- **Low salary is the strongest driver** — Employees earning up to $5K/month account for 163 of 237 attritions (~69%). 
- **The 26–35 age group is most vulnerable** — With 116 exits, this mid-career bracket is the highest-risk demographic segment.
- **Lab Technicians & Sales Executives need urgent focus** — These two roles alone contribute 119 of 237 attritions (~50% of total exits).
- **Life Sciences & Medical backgrounds dominate attrition** — Together they account for over 64% of attrition by education field. 
- **Single employees are significantly more likely to leave** — Singles represent 120 of 237 attritions.
- **Male attrition is nearly double female attrition** — 143 vs 80, warranting a gender-specific review of workload, growth, and pay equity.

---

## 📊 Dashboard Visuals

| Visual | Chart Type | What It Shows |
|---|---|---|
| KPI Summary Cards | Card tiles | Total Employees · Attrition Count · Rate · Avg Age · Avg Salary · Avg Tenure |
| Attrition by Gender | KPI Cards | Side-by-side Male (143) vs Female (80) attrition counts |
| Attrition by Education Field | Donut Chart | Share of attrition by educational background |
| Attrition by Age Group | Clustered Bar | Attrition count across five age brackets |
| Attrition by Job Role | Matrix Table | Attrition per role broken down by satisfaction level (1–4) with totals |
| Attrition by Salary Slab | Horizontal Bar | Attrition volume across four salary bands |
| Attrition by Years at Company | Area / Line Chart | Attrition trend over employee tenure (Year 0–15+) |
| Attrition by Marital Status | Horizontal Bar | Attrition count for Single, Married, and Divorced employees |

> All visuals support **department-level filtering** via slicers: `Human Resources` · `Research & Development` · `Sales`

---

## 🚀 How to Run This Project

### Prerequisites
- [Power BI Desktop](https://powerbi.microsoft.com/desktop/) — free download from Microsoft *(Windows only)*

### Steps

**1. Clone or download this repository**
```bash
git clone https://github.com/your-username/HR-Analytics-Dashboard.git
cd HR-Analytics-Dashboard
```

**2. Open the Power BI dashboard file**
- Launch Power BI Desktop
- Go to **File → Open** and select `HR_Analytics_Dashboard.pbix`

**3. Update the data source path**
- Go to **Home → Transform Data → Data Source Settings**
- Click **Change Source** and update the file path to `HR_Employee_Data.xlsx` on your local machine
- Click **Close & Apply**

**4. Refresh the data**
- Click **Home → Refresh** to reload all visuals

**5. Explore the dashboard**
- Use the department slicers at the top to filter by HR, R&D, or Sales
- Hover over any chart bar or segment for detailed tooltips

### 📁 Repository Structure

```
📂 HR-Analytics-Dashboard/
├── 📊 HR_Analytics_Dashboard.pbix    # Power BI dashboard file
├── 📋 HR_Employee_Data.xlsx          # Raw dataset (Excel)
├── 🖼️ Dashboard_preview.png          # Dashboard screenshot
└── 📄 README.md                      # Project documentation
```

---

## ✅ Results & Conclusion

This dashboard successfully identifies the key drivers of employee attrition:

- **Compensation is the single biggest lever** — nearly 70% of attrition comes from the lowest salary band ($0–5K/month)
- **Tenure risk follows a clear pattern** — attrition peaks sharply in Year 1 (59 exits), dips through mid-tenure, and rises again around Year 10
- **Role-specific concentration** in Lab Technicians and Sales Executives points to job-specific dissatisfaction or high external market demand for these skill sets
- **Demographic patterns** — young (26–35), single, male employees — define the highest-risk profile and should guide targeted retention strategies

> **Bottom line:** The organization can meaningfully reduce its **16.1% attrition rate** by prioritizing competitive entry-level compensation, a stronger first-year onboarding experience, and clear career growth pathways for high-attrition roles.

---

## 🔮 Future Work

- **Live HR Database Integration** — Replace the static Excel source with a live connection to an HR database (e.g., Azure SQL, SAP SuccessFactors, or Workday API) for real-time monitoring
- **Automated Alerts** — Configure Power BI data alerts to notify HR managers when attrition in any department exceeds a defined monthly threshold

---


