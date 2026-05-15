# Filters_to_SQL_Queries
- This repository contains my submission for the Google Cybersecurity Certificate activity following its given situation.

# Project description
- My organization is working to make their system more secure. It is my job to ensure the system is safe, investigate all potential security issues, and update employee computers as needed. The following steps provide examples of how I used SQL with filters to perform security-related tasks.

# Retrieve after hours failed login attempts
- A potential security incident occurred outside normal business hours (after 18:00), requiring an investigation into all unsuccessful login attempts made during that time.

- The following code shows how I created a SQL query to filter failed login attempts that took place after business hours.
<img width="975" height="210" alt="image" src="https://github.com/user-attachments/assets/6ece31ca-23df-4348-a2b6-28b5290158e9" />
- The first section of the screenshot displays my query, while the second section shows part of the resulting output. This query is designed to identify failed login attempts that occurred after 18:00. I began by selecting all records from the "log_in_attempts" table. Next, I applied a "WHERE" clause combined with an "AND" operator to filter the results so that only unsuccessful login attempts made after 18:00 were returned. The first condition, "login_time > '18:00'", filters for login attempts that took place after 18:00. The second condition, "success = FALSE", filters for login attempts that were unsuccessful.

# Retrieve login attempts on specific dates
- A suspicious event took place on 2022-05-09, requiring an investigation into all login activity that occurred on that date and the day prior.

- The following code demonstrates how I created a SQL query to filter login attempts that occurred on those specific dates.
<img width="975" height="210" alt="image" src="https://github.com/user-attachments/assets/36984d0b-7e4c-404c-994a-e68c46b5bf88" />
- This query retrieves all login attempts that occurred on either 2022-05-09 or 2022-05-08. I began by selecting all records from the "log_in_attempts" table. I then applied a "WHERE" clause with an OR operator to filter the results so that only login attempts from either of these two dates were included. The first condition, "login_date = '2022-05-09'", filters for logins that occurred on 2022-05-09. The second condition, "login_date = '2022-05-08'", filters for logins that occurred on 2022-05-08.

# Retrieve login attempts outside of Mexico
- After reviewing the organization’s login attempt data, I identified a potential issue involving login activity originating outside of Mexico. These attempts require further investigation.

- The following code demonstrates how I created a SQL query to filter for login attempts that occurred outside of Mexico.
<img width="975" height="210" alt="image" src="https://github.com/user-attachments/assets/799642ae-65b4-457c-8d77-12facd1df6be" />
- This query retrieves all login attempts that occurred in countries other than Mexico. I began by selecting all records from the "log_in_attempts" table. I then applied a "WHERE" clause using "NOT" to exclude results associated with Mexico. To account for variations in how Mexico is recorded in the dataset (such as MEX and MEXICO), I used the "LIKE" operator with the pattern MEX%. The % wildcard represents any number of characters, allowing the filter to match both formats.

# Retrieve employees in Marketing
- My team needs to update the computers used by certain employees in the Marketing department. To support this process, I first needed to identify which employee machines require updates.

- The following code demonstrates how I created a SQL query to filter for employee machines belonging to employees in the Marketing department located in the East building.
<img width="975" height="281" alt="image" src="https://github.com/user-attachments/assets/ec55932b-a404-4c01-a36b-a6a0b91cc1d5" />
- This query returns all employees in the Marketing department located in the East building. I began by selecting all records from the "`employees`" table. I then applied a "`WHERE`" clause using "`AND`" to filter the results so that only employees in the Marketing department and the East building were included. The first condition, "`department = 'Marketing'`", filters for employees in the Marketing department. The second condition, "`office LIKE 'East%'`", filters for employees assigned to the East building. I used the "`LIKE`" operator with the pattern "`East%`" because the office field includes additional details such as specific office numbers.

# Retrieve employees in Finance or Sales
- The machines used by employees in the Finance and Sales departments also require updates. Because these teams need a different security update, I needed to identify only employees within these two departments.

- The following code demonstrates how I created a SQL query to filter for employee machines belonging to employees in either the Finance or Sales departments.
<img width="975" height="271" alt="image" src="https://github.com/user-attachments/assets/617704b3-7589-4e7f-b10b-84e38bac4535" />
- This query returns all employees in the Finance and Sales departments. First, I started by selecting all data from the "employees" table. Then, I used a "WHERE" clause with "OR" to filter for employees who are in the Finance and Sales departments. I used the OR operator instead of AND because I want all employees who are in either department. The first condition is "department = 'Finance'", which filters for employees from the Finance department. The second condition is "department = 'Sales'", which filters for employees from the Sales department.

# Retrieve all employees not in IT
- My team needs to apply one additional security update for employees who are not part of the Information Technology department. To proceed with this update, I first needed to gather information on these employees.

- The following code demonstrates how I created a SQL query to filter for employee machines belonging to employees outside of the Information Technology department.
<img width="975" height="252" alt="image" src="https://github.com/user-attachments/assets/987e178b-9649-4a26-a73f-34f39a956f41" />
- This query returns all employees who are not part of the Information Technology department. I began by selecting all records from the "employees" table. I then applied a "WHERE" clause using "NOT" to exclude employees in the Information Technology department.

# Conclusion
- In conclusion, this activity demonstrated how SQL filters can be used to extract targeted and meaningful information from larger datasets. By working with the "log_in_attempts" and "employees" tables, I was able to apply different query conditions to support specific investigative and operational needs. Using logical operators such as "AND", "OR", and "NOT", along with the "LIKE" operator and "%" wildcard, allowed me to refine results and isolate relevant records efficiently. Overall, this exercise reinforced how structured queries can be used to analyze security-related data and support informed decision-making.

