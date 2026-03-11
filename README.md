# Employee_Attrition_Analysis
# Employee Attrition Analysis

## Overview
This project performs a comprehensive analysis of employee attrition using a provided Excel dataset. The primary goal is to identify patterns, correlations, and potential root causes of employee turnover, both at an organizational level and specifically for high-attrition job roles.

## Dataset
The analysis is based on the dataset: `Employee Attrition Analysis - Solution.xlsx`.

## Analysis Objectives
*   Load and perform initial exploration of the dataset.
*   Clean the data by handling missing values.
*   Analyze overall attrition patterns across various categorical variables (Department, Job Role, Over Time).
*   Visualize relationships between key numerical variables (Age vs. Monthly Income, Monthly Income Distribution by Department).
*   Conduct a deep dive into attrition within 'Sales Representatives', examining factors such as Over Time, Job Satisfaction, Environment Satisfaction, Work Life Balance, and Monthly Income.
*   Summarize all key findings and suggest actionable insights.

## Methodology
1.  **Data Loading & Initial Exploration**: Loaded the Excel file into a pandas DataFrame and used `df.info()` and `df.describe()` for an initial understanding of its structure and statistics.
2.  **Data Cleaning**: Addressed a single missing value in the 'Employee Number' column by dropping the corresponding row to maintain data integrity.
3.  **Overall Attrition Analysis**:
    *   Calculated and visualized attrition rates by 'Department', 'Job Role', and 'Over Time'.
    *   Used scatter plots to explore 'Age' vs. 'Monthly Income' and box plots for 'Monthly Income Distribution by Department'.
4.  **Deep Dive - Sales Representatives**:
    *   Filtered the dataset to focus solely on 'Sales Representative' roles.
    *   Analyzed attrition rates within this group based on 'Over Time', 'Job Satisfaction', 'Environment Satisfaction', 'Work Life Balance', and 'Monthly Income' through detailed tables and bar plots.
5.  **Code Refactoring**: Ensured all plotting code adhered to best practices and addressed `FutureWarning` messages from `seaborn` for cleaner outputs.

## Key Findings
### Overall Attrition Patterns:
*   **Departments**: 'Sales' (20.72%) and 'Human Resources' (19.05%) departments exhibited higher attrition rates compared to 'Research & Development' (13.81%).
*   **Job Roles**: 'Sales Representatives' (40.48%) showed the highest attrition, followed by 'Laboratory Technicians' (23.97%) and 'Human Resources' (23.08%). 'Managers' and 'Research Directors' had significantly lower rates.
*   **Over Time**: A strong correlation was found: employees working 'Over Time' had a 30.51% attrition rate, versus 10.49% for those not working overtime.
*   **Age & Income**: Attrited employees tended to be younger and had lower monthly incomes.

### Deep Dive: Sales Representatives Attrition:
*   **Over Time**: Sales Representatives working 'Over Time' faced an alarming 68.00% attrition rate, far exceeding the 28.81% for those not working overtime in the same role.
*   **Job Satisfaction**: Lower job satisfaction strongly correlated with higher attrition; Level 1 satisfaction led to 58.33% attrition.
*   **Environment Satisfaction**: While generally high, lower environment satisfaction (Level 1 at 45.45%) showed higher attrition, but rates were substantial across all levels.
*   **Work Life Balance**: An exceptionally high attrition rate (88.89%) was noted for those reporting 'Best' Work Life Balance (Level 4), though this finding requires caution due to a small sample size. Conversely, the 'Worst' balance (Level 1) showed 0% attrition (also small sample size).
*   **Monthly Income**: Attriting Sales Representatives generally had lower monthly incomes compared to those who stayed.

## Potential Root Causes and Recommendations
*   **Work-Life Balance Issues (Over Time)**: The most critical driver. Organizations should investigate reasons for overtime, optimize workloads, and ensure fair compensation to improve work-life balance.
*   **Job and Environment Satisfaction**: Enhance workplace conditions, provide professional development, and clarify career paths, especially for Sales and HR roles, to boost satisfaction.
*   **Compensation**: Review and ensure competitive compensation, particularly for Sales Representatives and younger employees, as lower income correlates with higher attrition.
*   **Role-Specific Stressors**: Conduct qualitative studies to understand the unique challenges faced by Sales Representatives and Laboratory Technicians that contribute to their high turnover.

## Next Steps / Further Exploration
*   Conduct qualitative interviews with attrited and current employees to gather deeper insights into satisfaction and work-life balance issues.
*   Analyze other factors like 'Years at Company', 'Years in Current Role', and 'Performance Rating' in relation to attrition.
*   Develop a predictive model for employee attrition based on the identified key features.
