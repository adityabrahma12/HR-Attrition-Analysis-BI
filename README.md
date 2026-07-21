# HR Analytics & Employee Attrition Strategy

A Power BI dashboard and statistical analysis of employee attrition across a 1,470-employee organization, extended with a multivariate regression model and an estimated financial impact of turnover — built to move beyond descriptive reporting into evidence-based retention strategy.

---

## 📌 Project Overview

Employee attrition carries costs well beyond recruitment fees — lost productivity, disrupted teams, and eroded institutional knowledge. This project analyzes a structured HR dataset to answer three questions for management:

1. **Where** is attrition concentrated — which departments, roles, salary bands, and tenure stages?
2. **Why** — which factors are *independently* responsible once confounding variables are controlled for, versus which are just correlated?
3. **So what** — what does this attrition actually cost the organization, and what should management do about it first?

The project combines an interactive Power BI dashboard with a statistical deep-dive (logistic regression) and a sourced financial impact estimate, delivered as a full management report.

---

## 🎯 Key Findings

| Metric | Value |
|---|---|
| Total Employees | 1,470 |
| Attrition Count | 237 |
| Attrition Rate | 16.1% |
| Average Age | 36.92 years |
| Average Monthly Salary | 6.50K |
| Average Tenure | 7.00 years |
| **Estimated Annualized Cost of Attrition** | **~$10.9M (≈9.4% of total payroll)** |

**Descriptive patterns** (from the dashboard):
- ~69% of exits come from the lowest salary bracket ("Upto 5k")
- Laboratory Technicians (62) and Sales Executives (57) are the highest-attrition job roles
- Attrition peaks sharply in the 26–35 age group and around the one-year tenure mark

**Statistically validated drivers** (from multivariate logistic regression, N=1,423, controlling for all variables simultaneously):
- **Overtime is the single strongest independent driver** (7.35× odds of attrition)
- Frequent business travel is the second-strongest driver (5.99× odds)
- Job involvement, job/environment satisfaction, work-life balance, and manager continuity are all statistically significant *protective* factors
- **Compensation is not a statistically significant independent predictor** once workload, travel, and engagement are controlled for (p = 0.79) — the raw salary pattern in the dashboard is real but confounded, since low pay clusters with high overtime and high-turnover roles in the same employees

This reframes the retention priority: **workload and role design, not pay alone, are the highest-leverage levers.**

---

## 🛠️ Tools & Methods

- **Microsoft Power BI** — dashboard design, DAX measures, department-level filtering
- **Python (pandas, statsmodels)** — data validation, multivariate logistic regression, odds-ratio analysis
- **Industry benchmarking** — SHRM 2025 Benchmarking Report and Gallup turnover research, used to translate attrition into an estimated financial impact

---

## 📁 Repository Contents

```
├── HR_Analytics.csv                     # Source dataset (1,470 employee records)
├── HR_Analytics_Project.pbix            # Power BI dashboard file
├── HR_Analytics_Strategic_Report.docx   # Full management report (findings + recommendations)
├── dashboard_preview.jpeg               # Dashboard screenshot
└── README.md
```

---

## 📊 Dashboard

The Power BI dashboard provides a single-page, filterable view of workforce composition and attrition drivers, with tabs for **Human Resources**, **Research & Development**, and **Sales**. It includes:

- Headline KPIs (headcount, attrition count/rate, average age/salary/tenure)
- Attrition by education field, age group, job role, salary slab, experience, and gender

To explore it interactively, open `HR_Analytics_Project.pbix` in [Power BI Desktop](https://www.microsoft.com/en-us/power-platform/products/power-bi/downloads).

---

## 📄 Full Report

`HR_Analytics_Strategic_Report.docx` contains the complete write-up, including:

1. Executive Summary
2. Introduction & Methodology
3. Dashboard Overview
4. Key Performance Indicators
5. Strategic Deep-Dive (descriptive segmentation)
6. **Multivariate Statistical Validation** of attrition drivers (logistic regression, odds ratios, significance testing)
7. **Estimated Financial Impact** of attrition (SHRM/Gallup-benchmarked replacement-cost model)
8. Recommendations for Management (prioritized by statistically validated impact)
9. Implementation Roadmap
10. Conclusion
11. Appendix (data dictionary, benchmark sources)

---

## 💡 Recommendations Summary

Prioritized by statistically validated impact rather than the strongest visual pattern on the dashboard:

1. **Overtime & workload rationalization** — highest-priority lever (7.35× odds)
2. **Redesign of frequent-travel roles**, concentrated in Sales
3. **Manager continuity & structured promotion cadence**
4. **Job involvement / engagement programs** (project ownership, recognition)
5. **Role-specific retention** for Sales Executives, Sales Representatives, Lab Technicians, and HR
6. Structured "stay interviews" at the 6- and 10-month tenure marks
7. Entry-level compensation review — reframed as a secondary, supporting lever rather than the primary fix

Full detail and evidence for each recommendation is in the report.

---

## ⚠️ Notes & Limitations

- The dataset is cross-sectional, not longitudinal — the regression identifies statistically significant associations, not proven causal direction.
- Several job-role subgroups have small sample sizes; their odds ratios should be treated as directional and revisited as more data accumulates.
- The financial impact estimate applies published industry benchmarks (SHRM, Gallup) to the dataset's salary figures. It is illustrative and should be validated against an organization's actual recruiting and vacancy-cost data before use in budget planning.

---

## 👤 Author

Prepared as an HR analytics and workforce strategy project, combining dashboard development with statistical modeling and financial impact analysis.
