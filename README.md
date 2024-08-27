# Census-2011-Analysis-using-SQL
This project involves analyzing the 2011 Census of India using SQL. It includes two datasets covering various demographic factors such as population, literacy rates, sex ratios, and growth rates across different states and districts .

# Key Findings:
1) SQL queries for data extraction and aggregation.
   
2) Analysis of literacy, sex ratio, and population growth.
 
3) Exploration of geographic and demographic relationships.
 
4) Custom queries for specific state and district-level insights.

First we need to create database then the table named dataset1 ,dataset2 and load data into them 
![Loading dataset1](https://github.com/user-attachments/assets/bab38b73-ada5-44ce-9366-b7a35c721575)
This query creates a table named dataset1 with columns to store the district name, state name, sex ratio, literacy rate, and population growth rate. The varchar type is used for text data (district and state names), int for the sex ratio (a whole number), and float for literacy and growth rates (which are decimal values).

Then we have a look at the data:
Dataset 1:
![Loading dataset1](https://github.com/user-attachments/assets/c4c516c8-188c-400b-a11c-277615df30fe)

Dataset2:
![Loading dataset2](https://github.com/user-attachments/assets/489dc39f-f7ee-4ca2-ad80-4096568a272a)

# Q1) Count the Number of Rows in the Datasets:
![Q1](https://github.com/user-attachments/assets/90a22d1c-70cc-43f0-bd5e-7fc4df08083f)
Explanation: These queries count the total number of rows in dataset1 and dataset2 using the count(*) function, which returns the total number of rows in each table.

# Q2) Data for Jharkhand and Bihar:
![Q2 A](https://github.com/user-attachments/assets/8abaf801-5a16-4c98-b739-afd3822184e5)
Explanation:These queries filter the data to show only the rows where the state column is either 'Jharkhand' or 'Bihar'. The IN clause allows for checking multiple values in the state column.
![Q2B](https://github.com/user-attachments/assets/9ee2dda6-5500-4cd7-b3be-e7ce9f22d1d9)

# Q3) Total Population of India:
![Q3](https://github.com/user-attachments/assets/6ccc8bbf-f42a-4cd5-a16a-347cb092817f)
Explanation: This query calculates the total population by summing up all values in the population column of dataset2. The sum() function adds together all the values in a column.

# Q4) Average Growth Rate:
![Q4](https://github.com/user-attachments/assets/b19b7e6f-69f7-4988-b879-2a68b9269b12)
Explanation: This query calculates the average growth rate across all entries in dataset1 using the avg() function. The result is labeled as result.

















