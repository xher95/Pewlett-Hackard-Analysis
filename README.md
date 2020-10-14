# Pewlett-Hackard-Analysis
## Problem
Pewlett-Hackard is a large company with thousands of employees, many whom will retire soon. We have to look at how many employees will retire soon, so we can enroll them in retirement packages and how many and what spots needs to be filled. Since Pewlett-Hackard has only been working with Excel and VDA, there are only six csv files. They have finally upgraded and we will no use SQL to create employee database to determine who will retire and how many spots must be filled.

## Steps and Challenges for Problem-Solving
1. Download and Install our tools
    - PostgresSQL
    - pgAdmin
2. Identify the data relationships
    - Organize our data with file folders
    - Dowload our databases
    - Inspect
    - Identify the database keys: primary key (pk) and foreign key (fk)
3. Determine the entity relationships by creating an entity relationships diagram (ERD)
    - Understand all of the data being inserted
    - Database components include tables, known as entities, with data, known as attributes
    - 3 types of ERDs: conceptual, logical, and physical
    - Quick DBD
      - helps with creating and visualizing diagrams
4. Launch pgAdmin and start creating tables
    - Use our ERD as reference to making out database tables
    - Codes used:
      - CREATE TABLE
      - NOT NULL
      - PRIMARY KEY
      - UNIQUE
    - Codes cannot be executed a second time because pgAdmin continuously runs the code unless told otherwise
    - Highlight the piece of code that you just want to run and run it
    - Import the data onto the tables
      - Right click the table and click Import/Export
      - Toggle to show Import, select CSV file, toggle Header to "YES," and select comma as Delimiter
      - Use code SELECT * FROM table_name to view the results
    - Importing errors will occur due to FOREIGN KEY constraints so you will need to import the data in a certain order
      - Googling other errors will help solve certain issues
5. Filter out the data that will include retirement eligibility
    - SELECT first_name, last_name
      FROM employees
      WHERE birth_date BETWEEN 'dates' AND 'dates'
    - This code was used to generate the possible employees who will retire, but the list was too big, so we added another filter to the code to filter the list even further
    - We used COUNT function to help calculate the sum of employees retiring
    - We use INNER JOIN, LEFT JOIN, RIGHT JOIN, and/or FULL OUTER JOIN to join our tables together to get the datas we wanted in one table
    - Add one more filter hire dates and birth dates

## Results of Analysis
The results of our Analysis isn't exactly clean yet because we are still left with questions such as repeat names under different department, but it did help narrow down our search for retirees.
### Limitations to Analysis
It seems we can only go as far as filtering certain data that is needed we are not able to know or identify repeat data that we come across our tables.
### Next Steps
We will contact our boss about the repeat data.
