# 🧾 HR Analytics Dashboard Project

## 📌 Objective
To analyze employee attrition patterns and identify factors influencing workforce stability using **Excel, SQL, Power BI, and Tableau**.

---

## 🧰 Tools Used
- **Microsoft Excel** – Data Cleaning & Dashboard Creation  
- **SQL** – Data Extraction, Transformation, and Analysis  
- **Power BI** – Interactive Dashboard with DAX and Slicers  
- **Tableau** – Advanced Data Visualization & Storytelling  

---

##  Key KPIs
1. Attrition Rate for All Departments  
2. Average Hourly Rate of Male Research Scientists  
3. Attrition Rate vs Monthly Income  
4. Average Working Years by Department  
5. Job Role vs Work-Life Balance  
6. Attrition Rate vs Years Since Last Promotion  

---

##  Dashboards
-  **Excel Dashboard:** Basic visual overview of attrition metrics.  
-  **Power BI Dashboard:** Interactive dashboard with slicers & DAX KPIs.  
-  **Tableau Dashboard:** Dynamic visualization and storytelling.  

---

##  SQL Highlights

SELECT Department, 
       COUNT(EmployeeID) AS Employee_Count,
       SUM(CASE WHEN Attrition = 'Yes' THEN 1 ELSE 0 END) AS Attrition_Count,
       ROUND(SUM(CASE WHEN Attrition = 'Yes' THEN 1 ELSE 0 END) * 100.0 / COUNT(EmployeeID), 2) AS Attrition_Rate
FROM HR_Combined
GROUP BY Department;



## Challenges & Solutions

###  Challenge 1: Combining Two HR Datasets
**Problem:** Two HR datasets had different column names and formats.  
**Solution:** Identified a common column (`Employee ID`), renamed headers for consistency, and merged them using **Power Query** and **SQL JOIN** operations.

---

###  Challenge 2: SQL Column Mismatch Errors During Import
**Problem:** When loading data into SQL, column headers didn’t match with the table schema.  
**Solution:** Adjusted table schema and data types using SQL commands such as:

ALTER TABLE HR_Combined
MODIFY COLUMN EmployeeID INT;

##  Key Insights
- Attrition is **higher in Sales and HR departments** compared to others.  
- Employees with **no promotion for long durations** are more likely to leave.  
- **Younger employees** tend to switch jobs more frequently for better opportunities.  
- **Work-life balance** has a strong impact on retention and overall satisfaction.  

---

## Conclusion
Focusing on **timely promotions**, **employee engagement**, and **fair compensation** can significantly reduce attrition.  
Encouraging **career growth**, **employee recognition**, and a **healthy work-life balance** will lead to improved retention and overall workforce satisfaction.  

---

## Author
**Ratnesh Ranjan Jha**  
*Data Analytics Intern @ Aivariant*  





##  Tags
`#PowerBI` `#SQL` `#Tableau` `#Excel` `#DataAnalytics` `#HRAnalytics`


