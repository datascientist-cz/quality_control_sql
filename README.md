# quality_control_sql
QUALITY CONTROL IN MANUFACTURING PROCESSES USING SPC

# Introduction: 
Manufacturing processes are similar to solving a complex puzzle, where each step plays a crucial role in ensuring that the final product meets quality standards. 
In this project, I carried out a simplified simulation of a process of monitoring and controlling production. The objective is to implement a method called Statistical Process Control (SPC). 
SPC leverages data to assess process performance, allowing adjustments only when measurements deviate from acceptable ranges. Through SQL analysis, we use historical manufacturing data to define control limits (upper and lower tolerance limits) and identify process anomalies to ensure that the quality of the products is consistent. 

# Data 
The dataset originates from a project sourced from DataCamp.

# Results 
The project leverages SQL's capabilities, employing various statements to achieve our goals:
1.	Common Table Expression (CTE): It is used to calculate moving averages (avg_height) and standard deviations (stddev_height) of product heights within a window spanning the current row and the preceding four rows. Window functions are used to ensure that the calculations are performed in a window that includes the previous 5 rows and the current row.
2.	Subquery: The main query incorporates a subquery to compute control limits (ucl and lcl) for each row. A WHERE clause is applied to filter out incomplete windows, ensuring accuracy in my analysis.
3.	Main Query: In the final query, I extracted the relevant columns from the subquery and I defined an alert status using a CASE statement. If a product's height exceeds the defined control limits, an alert is triggered. Conversely, products within the acceptable range are marked as such.

# Explanation
This project offers a compelling blend of window functions, subqueries, Common Table Expressions (CTEs), and conditional statements (CASE WHEN), simulating real-world manufacturing scenarios. 
In summary, this project is used to highlight the significance of data-driven decision-making in optimizing manufacturing operations. 

