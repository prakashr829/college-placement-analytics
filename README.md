# college-placement-analytics
Power BI dashboard analyzing student placement performance using academic and skill metrics
This Power BI dashboard analyzes student placement data to uncover the factors influencing campus recruitment outcomes. It visualizes how academic performance, IQ, internships, projects, and communication skills affect placement success.

Key Features
- Placement rate and performance KPIs  
- CGPA, IQ, and internship impact analysis

  
Column | Description |
|--------|--------------|
| College_ID | Unique student ID |
| IQ | Intelligence Quotient |
| CGPA | Cumulative Grade Point Average |
| Academic_Performance | Academic performance score |
| Internship_Experience | Internship exposure (Yes/No) |
| Communication_Skills | Rating for communication |
| Projects_Completed | Total projects completed |
| Placement | Placement status (Yes/No) | 


Tools Used
- **Power BI** – Data visualization  
- **DAX** – Measures and calculated columns  
- **Excel / CSV** – Data source


Sample DAX Measures
```DAX
Placed Students =
CALCULATE(
    DISTINCTCOUNT(CollegePlacement[College_ID]),
    CollegePlacement[Placement] = "Yes"
)

Placement Rate (%) =
DIVIDE([Placed Students], DISTINCTCOUNT(CollegePlacement[College_ID]), 0)
