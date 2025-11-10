# README
# Project: Analyzing Employee Trends using Tableau

## Project Overview
This project analyzes employee-related data and presents the results through an interactive Tableau dashboard. The dashboard visualizes workforce distribution by department, education level, education field, gender, business travel frequency, marital status, and job satisfaction. The purpose is to provide HR and management with actionable insights for workforce planning, training, and policy decisions.

## Objectives
1. Analyze employee distribution across departments and education levels.
2. Provide visual insights into gender ratio and business travel patterns.
3. Compare education fields with average job satisfaction.
4. Present quick summary metrics such as Total Employees and Active Employees.
5. Build an interactive dashboard with filters for granular analysis.
6. Enable data-driven decision making for HR management.

## Dataset
- Filename: `Analyzing Employee Trends.csv`
- Description: The CSV contains employee records with attributes including (but not limited to):
  - EmployeeID
  - Department
  - Gender
  - Education
  - EducationField
  - JobSatisfaction
  - BusinessTravel
  - MaritalStatus
  - Status (or similar field indicating active/inactive)
- Note: Ensure the dataset is cleaned and columns are standardized before importing into Tableau.

## Files Included
- `Analyzing Employee Trends.csv` — primary dataset used for the dashboard.
- `Analyzing Employee Trends.twbx` — Tableau packaged workbook (dashboard).
- `Tableau Dashboard.png` — screenshot of the dashboard (for documentation).
- `Project Report.docx` (optional) — formatted report ready for submission.
- `README.txt` or `README.md` — this file.

## Prerequisites
- Tableau Desktop (or Tableau Public) installed.
- Access to the provided CSV dataset.
- Basic familiarity with Tableau interface (shelves, marks, filters, calculated fields).

## Installation / Setup Instructions
1. Copy the repository folder to your local machine.
2. Open Tableau Desktop.
3. From the start screen, click **"Text File"** and select `Analyzing Employee Trends.csv`.
4. Verify field types (string, date, integer, etc.) and rename columns for readability if necessary.
5. Save the cleaned data source as part of the workbook, or publish it to Tableau Server if required.

## How to Open the Dashboard
1. Open `Analyzing Employee Trends.twbx` in Tableau Desktop.
2. Navigate to the “Dashboard” tab to view the assembled dashboard layout.
3. Use the filters on the right-hand panel (Marital Status, Gender) to interactively filter visualizations.
4. Click on bars, tree map segments, or pie sections to cross-filter other charts on the dashboard.

## Dashboard Components and Interpretation
- **Department-wise Employee Count (Bar Chart):**
  - Shows the number of employees per department (R&D, Sales, HR).
  - Use: Understand departmental headcount and resource allocation.

- **Type of Degree (Tree Map):**
  - Visualizes distribution of education levels (High School, Associate, Bachelor, Master).
  - Use: Assess qualification levels of the workforce.

- **Gender Distribution (Pie Chart):**
  - Displays proportion of male and female employees.
  - Use: Quick view of gender balance in the organization.

- **Education Field vs Average Job Satisfaction (Dual Axis Chart):**
  - Bars indicate number of employees per education field; the line shows average job satisfaction for each field.
  - Use: Identify which education backgrounds correspond to higher or lower satisfaction.

- **Business Travel (Text Table / Summary):**
  - Shows counts for Travel_Frequently, Travel_Rarely, Non-Travel.
  - Use: Plan travel budgets and evaluate workload.

- **Summary Cards (KPI Cards):**
  - **Total Employees**: Count of all employee records in the dataset.
  - **Active Employees**: Count of employees currently active (based on a Status field).
  - Use: Instant overview of workforce size and currently employed staff.

## How Total Employees and Active Employees are Defined
- **Total Employees**: The total number of rows/records in the dataset representing employees (historical + current if dataset contains historical records).
- **Active Employees**: Subset of Total Employees where a field (e.g., `Status`) indicates the employee is currently employed (e.g., `Status = Active` or `IsActive = Yes`).

## Steps to Recreate Key Visuals (short guide)
1. Department Bar Chart:
   - Drag `Department` to Rows.
   - Drag `Number of Records` (or `EmployeeID` count) to Columns.
   - Sort descending and add labels.

2. Education Tree Map:
   - Drag `Education` to Detail.
   - Drag `Number of Records` to Size and Label.
   - Select Chart Type -> Treemap.

3. Gender Pie Chart:
   - Drag `Gender` to Color and Label.
   - Drag `Number of Records` to Angle.
   - Select Pie Chart from Show Me.

4. Dual Axis Chart (Education Field vs Job Satisfaction):
   - Create a bar chart with `EducationField` on Rows and `Number of Records` on Columns.
   - Create a line chart with `EducationField` on Rows and `AVG(JobSatisfaction)` on Columns.
   - Combine as dual axis and synchronize if needed.

5. KPI Cards:
   - Create calculated fields for Total and Active counts or use `Number of Records` with appropriate filters.
   - Use the Text object or KPI tile to display values prominently.

## Data Cleaning Notes
- Ensure consistent category names (e.g., `Travel_Rarely` not `Travel Rarely`).
- Convert numeric satisfaction scales to numeric type if imported as string.
- Remove duplicate employee records if they exist (based on EmployeeID).
- Handle missing values for critical fields (e.g., `JobSatisfaction`) before computing averages.

## Limitations
- The analysis depends on the completeness and accuracy of the CSV dataset.
- If the dataset contains historical records (employees who left), Total Employees may not represent current workforce unless filtered.
- Job satisfaction is an average metric and may not capture all nuances of employee sentiment.

## Future Enhancements
1. Connect Tableau workbook to a live HR database for real-time updates.
2. Add additional metrics such as salary, performance rating, tenure, and promotions.
3. Implement predictive analytics (attrition prediction, satisfaction forecasting).
4. Create departmental drill-down dashboards for detailed operational insights.
5. Embed dashboards into an internal HR portal or Tableau Server for secure sharing.

## Documentation and Screenshots
- Insert the following screenshots into the report or documentation:
  - `Figure 1`: Main Dashboard Overview (full layout)
  - `Figure 2`: Education Field vs Job Satisfaction (close-up)
  - `Figure 3`: Department Bar Chart and Gender Pie Chart
  - `Figure 4`: KPI Cards showing Total vs Active Employees
- Each figure should have a short caption and a 1–2 sentence explanation.

## Citation and References
- Tableau Documentation: https://www.tableau.com/learn
- Dataset source: `Analyzing Employee Trends.csv` (include original source if applicable)
- Any external references or course materials used during analysis

## Author and Contact
- Author: Komal Kaim (MCA Student)
- Institution: [Your College / Department]
- Email: [Your Email Address]

## License (Optional)
- This project is for academic use. Reuse and redistribution should include attribution to the author.

