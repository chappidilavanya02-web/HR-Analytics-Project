# Key Findings – HR Employee Attrition Analysis

## 1. Overall Workforce Overview

The dataset contains 1,470 employee records.

| Metric | Result |
|---|---:|
| Total Employees | 1,470 |
| Employees Who Left | 237 |
| Active Employees | 1,233 |
| Attrition Rate | 16.1% |
| Retention Rate | 83.9% |

The overall attrition rate is approximately 16.1%, meaning around one in six employees in this dataset left the organisation.

## 2. Attrition by Department

| Department | Employees | Attrition Count | Attrition Rate |
|---|---:|---:|---:|
| Research & Development | 961 | 133 | 13.8% |
| Sales | 446 | 92 | 20.6% |
| Human Resources | 63 | 12 | 19.0% |

**Finding:** Sales has the highest attrition rate among the three departments, at 20.6%. Research & Development has the lowest rate, at 13.8%.

## 3. Attrition by Age Group

| Age Group | Employees | Attrition Count | Attrition Rate |
|---|---:|---:|---:|
| 18–25 | 123 | 44 | 35.8% |
| 26–35 | 606 | 116 | 19.1% |
| 36–45 | 468 | 43 | 9.2% |
| 46–55 | 226 | 26 | 11.5% |
| 56+ | 47 | 8 | 17.0% |

**Finding:** Employees aged 18–25 have the highest attrition rate, at 35.8%. The 36–45 age group has the lowest rate, at 9.2%.

## 4. Attrition by Gender

| Gender | Employees | Attrition Count | Attrition Rate |
|---|---:|---:|---:|
| Female | 588 | 87 | 14.8% |
| Male | 882 | 150 | 17.0% |

**Finding:** The attrition rate is slightly higher among male employees than female employees. This difference should not be treated as statistically significant without further testing.

## 5. Attrition by Business Travel

| Business Travel | Employees | Attrition Count | Attrition Rate |
|---|---:|---:|---:|
| Non-Travel | 150 | 12 | 8.0% |
| Travel Rarely | 1,043 | 156 | 15.0% |
| Travel Frequently | 277 | 69 | 24.9% |

**Finding:** Employees who travel frequently have a higher attrition rate of 24.9%, compared with 8.0% among employees who do not travel.

## 6. Attrition by Job Role

| Job Role | Employees | Attrition Rate |
|---|---:|---:|
| Sales Representative | 83 | 39.8% |
| Laboratory Technician | 259 | 23.9% |
| Human Resources | 52 | 23.1% |
| Sales Executive | 326 | 17.5% |
| Research Scientist | 292 | 16.1% |
| Healthcare Representative | 131 | 6.9% |
| Manufacturing Director | 145 | 6.9% |
| Manager | 102 | 4.9% |
| Research Director | 80 | 2.5% |

**Finding:** Sales Representatives have the highest attrition rate, followed by Laboratory Technicians and Human Resources roles. Manager and Research Director roles have comparatively low attrition rates.

## 7. Attrition by Overtime

| Overtime | Employees | Attrition Rate |
|---|---:|---:|
| Yes | 416 | 30.5% |
| No | 1,054 | 10.4% |

**Finding:** Employees working overtime have an attrition rate approximately three times higher than employees who do not work overtime.

This is a strong association in the dataset, but it does not establish that overtime directly causes employees to leave.

## 8. Attrition by Income Band

| Monthly Income Band | Employees | Attrition Rate |
|---|---:|---:|
| Below 3,000 | 395 | 28.6% |
| 3,000–6,000 | 519 | 12.7% |
| 6,000–10,000 | 275 | 12.0% |
| Above 10,000 | 281 | 8.9% |

**Finding:** The lowest income band has the highest attrition rate, at 28.6%. The highest income band has the lowest rate, at 8.9%.

Average monthly income:
- Employees who left: approximately 4,787
- Employees who stayed: approximately 6,833
- Overall average: approximately 6,503

This indicates an association between lower income and higher attrition in this dataset. It does not prove that compensation alone explains employee exits.

## 9. Attrition by Job Satisfaction and Work-Life Balance

### Job Satisfaction

| Satisfaction Level | Attrition Rate |
|---|---:|
| 1 | 22.8% |
| 2 | 16.4% |
| 3 | 16.5% |
| 4 | 11.3% |

Employees reporting the lowest job satisfaction have the highest attrition rate.

### Work-Life Balance

| Work-Life Balance Level | Attrition Rate |
|---|---:|
| 1 | 31.2% |
| 2 | 16.9% |
| 3 | 14.2% |
| 4 | 17.6% |

The lowest work-life balance category has the highest attrition rate. The pattern is not perfectly linear across all categories.

## 10. Attrition by Tenure and Experience

### Years at Company

| Tenure Band | Attrition Rate |
|---|---:|
| 0–1 years | 34.9% |
| 2–5 years | 15.5% |
| 6–10 years | 12.3% |
| 11–20 years | 6.7% |
| 21+ years | 12.1% |

Employees in their first year at the company have the highest attrition rate.

### Years in Current Role

| Role Tenure Band | Attrition Rate |
|---|---:|
| 0–1 years | 27.9% |
| 2–3 years | 16.6% |
| 4–7 years | 12.3% |
| 8+ years | 7.6% |

Attrition generally decreases as time in the current role increases.

### Total Work Experience

| Experience Band | Attrition Rate |
|---|---:|
| 0–5 years | 28.8% |
| 6–10 years | 15.0% |
| 11–20 years | 11.5% |
| 21+ years | 7.7% |

Employees with less total work experience have higher attrition rates in this dataset.

### Years Since Last Promotion

| Promotion Band | Attrition Rate |
|---|---:|
| 0 years | 18.9% |
| 1–2 years | 14.7% |
| 3–5 years | 10.1% |
| 6+ years | 16.3% |

The pattern is not consistently increasing or decreasing. Therefore, the results do not support a simple conclusion that longer time since promotion always leads to higher attrition.

## 11. Main Business Insights

The analysis highlights several patterns that HR teams could investigate further:

1. **Overtime:** Employees working overtime show substantially higher attrition.
2. **Early-career employees:** Younger employees and employees with less work experience show higher attrition.
3. **First-year employees:** The first year at the company has the highest attrition rate among the company-tenure groups.
4. **Job roles:** Sales Representatives and Laboratory Technicians have relatively high attrition.
5. **Business travel:** Frequent travellers show higher attrition than employees who do not travel.
6. **Compensation:** Lower income groups show higher attrition.
7. **Employee satisfaction:** Low job satisfaction and low work-life balance are associated with higher attrition.

## 12. Recommendations

Based on these observed patterns, the following areas could be investigated:

- Review overtime practices and workload distribution.
- Strengthen onboarding and first-year employee support.
- Examine attrition patterns in Sales and Laboratory Technician roles.
- Review travel demands for frequently travelling employees.
- Examine compensation structures in lower income groups.
- Investigate employee satisfaction and work-life balance concerns.

These are investigation priorities, not proven solutions.

## 13. Limitations

- The dataset is a public IBM HR sample and does not necessarily represent a real organisation.
- The dataset is a single snapshot and does not include employee exit dates or longitudinal employment history.
- The retention rate represents the proportion currently marked as active in this dataset; it is not a period-based retention metric.
- The analysis identifies associations, not causal relationships.
- Some employee groups have small sample sizes, which can make their attrition rates less stable.
- No statistical significance testing was performed.
- Employee age, income and tenure bands use analyst-defined cut-offs.

## 14. Conclusion

The analysis identifies overtime, early-career and early-tenure status, job role, business travel, income and employee satisfaction as characteristics associated with different attrition rates.

The findings provide a starting point for further HR investigation and demonstrate how Python and Power BI can be used to assess workforce patterns and communicate analytical insights.
