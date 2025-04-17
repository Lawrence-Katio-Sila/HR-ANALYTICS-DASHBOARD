
# JUBILYTE HR ANALYTICS 

## Problem Statement
This Power BI dashboard analyzes hr data from jubilyte company, focusing on employee attrition, demographics, job satisfaction, and department performance. The project helps  jubilyte hr managers identify workforce patterns and make data-driven decisions.

### Software Used
- Power query -> Data cleaning and transformation
- Powerbi -> Data modeling, DAX calculations and interactive visualizations.
- DAX -> Calculated measures and KPIs

### Steps Followed
- Step 1 : Obtained the hr dataset in excel file format from jubilyte company.
- Step 2 :Open power query editor and reviewed the raw data to check "column distribution", "column quality" and understand its structure, key columns, and potential quality issues (for example the missing values and inconsistent formatting).
- Step 3 : Also since by default, profile will be opened only for 1000 rows, you need to select "column profiling based on the entire dataset".
- Step 4 :  In power query unnecessary columns were removed and renamed for clarity and consistency.
- Step 5 : Handled missing values and null values appropriately.
- Step 6 : Converted data types (e.g, date, number, text) to match analysis needs.
- Step 7 : Created age group categories using conditional formatting below in power query;

       (1.1) 97 of the employees belong to"Under 25" age group,

       (1.2) 554 of the employees belong to "25–34" age group,

       (1.3) 505 of the employees belong to "35–44" age group,

       (1.4) 245 of the employees belong to "45–54" age group,

       (1.5) 69 of the employees belong to "Over 55" age group.

       Screenshot of different age groups by conditional formatting

       ![Image](https://github.com/user-attachments/assets/92d8a7d7-d601-43e4-968a-cf43e1236fc5)
- Step 8 : Ensured column headers and data were properly structured before closing and applying to load the dataset to Power BI.
- Step 9 : Loaded the cleaned dataset into Power BI for modeling and visualization.
- Step 10 : Created and calculated meaningful DAX measures to track business KPIs.
      The folowing DAX measures expression were written:

   (a) Overall employees = COUNTROWS('HR data')

  Screenshot of overall employee count formula;

  ![Image](https://github.com/user-attachments/assets/60d5273f-007f-489f-9298-536820ef3f95)

  (b) Attrition  = CALCULATE(COUNTROWS('HR data'), 'HR data'[attrition] = "Yes")

   Screenshot of attrition formula;

  ![Image](https://github.com/user-attachments/assets/3c90f88d-512d-47bb-a1bb-222b400bba83)
   
   (c) Attrition rate = DIVIDE([Attrition Employees], [Overall Employees], 0)
  
   Screenshot of attrition rate formula;
  
  ![Image](https://github.com/user-attachments/assets/03c0d260-b203-4072-afcb-1b33d7acaffd)

   (d) Active count = CALCULATE(COUNTROWS('HR data'), 'HR data'[attrition] = "No")
  
   Screenshot of Active employees formula;
  
  ![Image](https://github.com/user-attachments/assets/e45e54ef-0471-4068-9a3c-d1b6e3e70283)

   (e) Average Age (changed dataset from sum of age to average in the field settings)

- Steps 11 : In the report view 5 card visuals(kpis) were added to the canvas to display the total number of employees, attrition count, attrition rate, active count and average age respectively.

  Screenshot of KPIs chart was added;

  ![Image](https://github.com/user-attachments/assets/0d1d8cb1-50be-481b-9927-dc0f9df9c283)

- Step 12 : In the report view Visual filters(slicers) were added for 5 fields named "associate degree", "bachelor degree", "doctorate degree", "high school" and "masters degree")

  Screenshot of the slicers(filters) chart was added;

  ![Image](https://github.com/user-attachments/assets/aacdb48e-1f46-4fc7-99da-9827ae6b55fb)

- Step 13 : A pie chart was used to represent attrition by department (R&D), sales, HR) to quickly see which department had the most leavers.

  Screenshot of department attrition chart was added;

  ![Image](https://github.com/user-attachments/assets/4b6175fa-1356-4774-b4aa-8bc51b4a66ed)

- Step 14 : A stacked column chart was used to analyze number of employees by age group,while creating this visual, field named gender was also added to the legend bucket, thus the number of employees are also seggregated according to gender using colour coding and applied conditional formatting to visually categorize each age group.

  Screenshot of number of employees by age group chart was added;

  ![Image](https://github.com/user-attachments/assets/6bb2f1c1-57ba-4b2a-b149-5ff291ecc16e)

- Step 15 : A matrix chart was used to showcase job satisfaction across job roles in the report view area to observe where satisfaction was high or low.

  Screenshot of job satisfactory rating chart was added;

  ![Image](https://github.com/user-attachments/assets/9e7444be-3a28-4e8b-8e55-61b9b211d552)

- Step 16 : A stacked bar chart was used to highlight attrition by education field to identify which educational backgrounds had higher turnover rates.

  Screenshot of education wise attrition chart was added;

  ![Image](https://github.com/user-attachments/assets/14f7f11c-d246-488f-be04-2fb4fb836fd8)

- Step 17 : Displayed gender wise Attrition for different age group using five  donut charts and complemented each donut chart with a card visual indicating the number of attrition in that age category:

      (2.1) 38 of the attrition employees belongs to "Under 25" age group,

      (2.2) 112 of the attrition employees belongs to "25–34" age group,

      (2.3) 51 of the attrition employees belongs to "35–44" age group,

      (2.4) 25 of the attrition employees belongs to "45–54" age group,

      (2.5) 11 of the attrition employees belongs to "Over 55" age group.

   Screenshot of  attrition rate for different age groups by gender chart was added;

   ![Image](https://github.com/user-attachments/assets/7ed36d59-bde3-421f-9aea-de244759f3c8)

- Step 18 : The report was then published to Power BI Service.

  # Screenshot of Dashboard (Powerbi Service)

   ![Image](https://github.com/user-attachments/assets/982dfe4b-291f-4087-8860-ef23d29efb17)

# Insights
A single page report was created on Power BI desktop & it was the published to Power BI Service,

Following inferences can be drawn from the dashboard;
### [1] High Attrition Rate

- The company has an overall attrition rate of 16.12% with 237 employees having left the organization.
  

- This is a significant number and indicates a need for further investigation into retention strategies.

### [2] Departments Most Affected by Attrition

- R&D Department faces the highest attrition (56%), followed by sales (39%) and HR (5%).

- Targeted interventions may be required in R&D and Sales  departments to understand the causes and improve retention.

### [3] Age Group Trends

- The age group between 25-34 has the highest number of attrition employees (112), followed by age group between 35-44 which has(51)  attrition employees.

- Younger age groups, especially Under 25 which falls between(38)employees, may be more likely to leave, based on attrition donut charts by age.
  
### [4] Gender Disparity in Attrition

- Donut charts show differences in attrition rates between male and female employees across age groups.

- These disparities could point to gender related workplace issues or lifestyle based decisions and should be explored further.
- 
### [5] Education Field Influence on Attrition

- Employees with a background in Life Sciences (89) and Medical (63) have the highest attrition.

- On the other hand, fields like Human Resources (7 employees) and Other (11 employees) have much lower attrition.

### [6] Job Satisfaction Rating Analysis

- The matrix chart reveals job satisfaction levels across various job roles.

- Roles with consistently lower satisfaction ratings could be contributing to the attrition numbers.

### [7] Balanced Workforce Gender Distribution by Age Group

- The stacked column chart shows a fairly balanced distribution of male and female employees across age groups.

- This balance is a positive sign for diversity but should be monitored in relation to attrition trends.














                    
 
