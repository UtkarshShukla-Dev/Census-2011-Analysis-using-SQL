# Census-2011-Analysis-using-SQL
This project involves analyzing the 2011 Census of India using SQL. It includes two datasets covering various demographic factors such as population, literacy rates, sex ratios, and growth rates across different states and districts .
We are using PostgreSQL for Analysis .

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

# Q5) Average Growth Rate per State:
![Q5](https://github.com/user-attachments/assets/85ad13ae-a55f-4311-b42b-4ef3abc8857c)
Explanation: This query calculates the average growth rate for each state by grouping the data by state. The results are ordered in descending order by the average growth rate (result).

# Q6) Average Sex Ratio by State:
![Q7](https://github.com/user-attachments/assets/28ea6081-488a-4c1e-9051-d64b754df530)
Explanation: This query calculates the average sex ratio for each state. The avg() function calculates the average, and round() rounds the result to the nearest whole number. The states are ordered by the average sex ratio in descending order.

# Q7) Average Literacy by State:
![Q7](https://github.com/user-attachments/assets/308ca153-f6c7-4428-81c0-f8cb1b536717)
Explanation: This query calculates the average literacy rate for each state. The avg() function computes the average, and ROUND() combined with CAST() converts the result to a numeric value and rounds it to the nearest whole number. The states are then ordered by the literacy rate in descending order.

# Q8 A)  Sort States and Districts by Literacy Rate:
![Q8A](https://github.com/user-attachments/assets/90e1e450-b52d-4756-b4d3-7bedefa84b08)
Explanation: This query finds the maximum literacy rate for each state and district, grouping by both the state and district columns. The results are then sorted in descending order by the maximum literacy rate.

# Q8 B)  States with Average Literacy > 90:
![Q8B](https://github.com/user-attachments/assets/6542636f-7afc-4957-a353-bd88a41ff810)
Explanation: This query filters the states to include only those with an average literacy rate greater than 90%. The HAVING clause is used here to filter groups based on the calculated average literacy rate, after grouping by state.

# Q9)  States Starting with Letter A:
![Q9](https://github.com/user-attachments/assets/5eaa49c1-7872-403c-8992-058609c437ea)
Explanation: This query selects distinct states whose names start with the letter 'A'. The LIKE 'A%' pattern matches any string that begins with 'A', followed by any number of characters.

# Q10) States Ending with Letter a:
![Q10](https://github.com/user-attachments/assets/293e346f-2a8a-4573-8667-32a49c109a4d)
Explanation: This query selects distinct states whose names end with the letter 'a'. The LIKE '%a' pattern matches any string that ends with 'a', preceded by any number of characters.

# Q11) List of States and Districts with Total Area:
![Q11](https://github.com/user-attachments/assets/08bd3588-00c4-43ac-bb8f-e6cb663482a1)
Explanation: This query joins dataset1 and dataset2 on the state column. It then groups the data by state and district and sums the area for each combination. The results are ordered by the total area in descending order.

# Q12) Relation Between Literacy and Area:
![Q12](https://github.com/user-attachments/assets/c7c28d22-ff85-4c49-8824-e463b958d8d8)

Explanation: This query analyzes the relationship between literacy and area by selecting data from both dataset1 and dataset2 (joined on the state column). The data is ordered by literacy in descending order.

# Q13) Relation Between Sex Ratio and Area:
![Q13](https://github.com/user-attachments/assets/fe9f3ff6-d453-47dc-8dc9-85048174ec57)
Explanation: This query analyzes the relationship between sex ratio and area by joining dataset1 and dataset2 on the state column. The data is ordered by sex ratio in descending order.

# Q14) Relation Between Growth of Population and Area:
![Q14](https://github.com/user-attachments/assets/538f0976-2b48-41b6-b026-5ffb931b97c3)
Explanation: This query analyzes the relationship between population growth and area by joining dataset1 and dataset2 on the state column. The data is ordered by growth rate in descending order.
































