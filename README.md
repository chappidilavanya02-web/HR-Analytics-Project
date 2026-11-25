# HR Employee Attrition Analysis | Python & Power BI

An end-to-end HR Analytics project exploring employee attrition patterns, workforce characteristics, compensation, job satisfaction and employee tenure using Python and Power BI.

## 📊 Power BI Dashboard Preview

### 1. HR Overview

![HR Overview](Screenshots/HR_Overview.png)

### 2. Employee Attrition Analysis

![Employee Attrition Analysis](Screenshots/Employee_Attrition_Analysis.png)

### 3. Employee Retention Analysis

![Employee Retention Analysis](Screenshots/Employee_Retention_Analysis.png)

---

## Project Overview

Employee attrition is an important workforce challenge for organisations. This project analyses employee-level HR data to understand attrition patterns and identify workforce characteristics associated with employees leaving an organisation.

The project uses Python for data inspection, data quality assessment and cleaning, and Power BI for interactive reporting and visualisation.

## Business Questions

- What proportion of employees have left the organisation?
- Which departments and job roles have higher attrition?
- How does attrition vary across age groups and employee experience?
- How are overtime and monthly income associated with attrition?
- How do job satisfaction and work-life balance relate to attrition?
- How does attrition vary across employee tenure and promotion history?

See [Business Questions](Documentation/Business_Questions.md).

## Key Findings

- Overall employee attrition rate is approximately **16.1%**.
- Sales has a higher attrition rate than the other departments.
- Employees working overtime have a higher attrition rate than employees who do not.
- Employees aged 18–25 show a relatively high attrition rate.
- Sales Representatives have the highest attrition rate among the job roles.
- Employees in the lowest monthly income band show higher attrition than those in the highest band.
- Employees in their first year at the company show a high attrition rate.

See [Key Findings](Documentation/Key_Findings.md) for detailed results.

## Tools and Technologies

- **Python:** Data analysis and preparation
- **Pandas:** Data manipulation and cleaning
- **NumPy:** Numerical operations
- **Matplotlib & Seaborn:** Data visualisation
- **Jupyter Notebook:** Exploratory data analysis
- **Power BI:** Interactive dashboard development
- **DAX:** Measures and calculated columns

## Project Workflow

1. Loaded and inspected the raw HR dataset.
2. Performed data quality assessment.
3. Analysed categorical distributions and numerical ranges.
4. Investigated potential statistical outliers.
5. Performed business rule validation.
6. Cleaned and prepared the dataset.
7. Exported the cleaned dataset.
8. Created DAX measures and calculated columns in Power BI.
9. Developed three interactive dashboard pages.
10. Validated dashboard results against the dataset.

## Dashboard Pages

| Page | Purpose |
|---|---|
| HR Overview | Overall workforce metrics and attrition patterns |
| Employee Attrition Analysis | Attrition across job roles, overtime, income and employee characteristics |
| Employee Retention Analysis | Attrition patterns across tenure, experience and promotion history |

## Dataset

This project uses the IBM HR Employee Attrition dataset.

The dataset contains **1,470 employee records and 35 original columns**.

The cleaned analytical dataset contains 32 columns after removing three constant-value columns that did not contribute to the analysis.

The original dataset is not included in this repository. Refer to the dataset source and usage terms before downloading or redistributing it.

## Project Documentation

- [Business Questions](Documentation/Business_Questions.md)
- [Data Cleaning](Documentation/Data_Cleaning.md)
- [Key Findings](Documentation/Key_Findings.md)

## Limitations

- The dataset is a public sample and does not represent a specific real-world organisation.
- The data represents a single snapshot rather than a longitudinal employee history.
- Attrition patterns indicate associations, not proven causes.
- The dataset does not support true time-based retention or survival analysis.
- Income currency is not specified in the analysis, so income values are presented in the dataset's original units.

## Conclusion

This project demonstrates an end-to-end HR analytics workflow, from data quality assessment and preparation in Python to interactive reporting in Power BI.

The analysis highlights workforce groups and characteristics that may warrant further investigation by HR stakeholders.
