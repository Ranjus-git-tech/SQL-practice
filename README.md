# Student Database SQL Practice

This repository contains my practice work with SQL basics using a simple **Student Database**.  
I used this project to learn and experiment with essential SQL concepts such as table creation, constraints, data manipulation, and queries.

---

## 📚 Topics Covered

- **Database Schema**
  - Creating tables
  - Adding & dropping columns
  - Constraints: `PRIMARY KEY`, `UNIQUE`, `NOT NULL`, `DEFAULT`, `AUTO_INCREMENT`

- **Data Manipulation (DML)**
  - `INSERT`
  - `UPDATE`
  - `DELETE`

- **Filtering Data**
  - `WHERE`, `AND`, `OR`, `IN`, `NOT IN`, `<>`
  - Comparisons (`<`, `<=`, `>`)

- **Sorting & Limiting**
  - `ORDER BY`
  - `LIMIT`

- **Other Operations**
  - Updating multiple records
  - Deleting specific rows
  - Resetting IDs
 
  - updates will be added in the future as I grow more familiar with SQL.
 

# Office Database (MySQL)

This project contains a sample **Office Database** implemented in MySQL.  
It models employees, branches, clients, suppliers, and their relationships, inspired by *The Office*.  

---

## 📂 Contents
- **`office_db.sql`** – Full SQL script including:
  - Table creation with relationships and constraints
  - Sample data inserts
  - Updates to link managers and employees
  - Example queries (ordering, aggregation, wildcards, unions, joins, nested queries)

- **`README.md`** – Project documentation

---

## 🗄️ Database Schema
The database consists of the following tables:
- **employee** – Employee details, salaries, managers, and branches
- **branch** – Branch information and managers
- **client** – Clients associated with branches
- **works_with** – Sales between employees and clients
- **branch_supplier** – Suppliers linked to branches

Office Database with MySQL Triggers

This repository contains a MySQL schema for an Office Management Database, complete with relationships, sample data, queries, and triggers for logging events.

📂 Contents

office_db_with_triggers.sql → Main SQL script (tables, sample data, triggers).

README.md → Project documentation.

🗄️ Database Schema

The database models an office environment with the following tables:

employee → Employee details (ID, name, DOB, salary, supervisor, branch).

branch → Branch details and manager info.

client → Client information tied to branches.

works_with → Tracks sales between employees and clients.

branch_supplier → Supplier information linked to branches.

data_stamp → Audit log for new employee insertions.

sex_stamp → Audit log for gender-specific employee insertions.

⚡ Triggers

Two triggers have been implemented:

data_stamp_trigger → Logs "Added new employee" into data_stamp when a new employee is inserted.

sex_stamp_trigger → Logs gender-specific messages into sex_stamp:

"Added male employee"

"Added female employee"

"Added employee with unspecified sex"

🚀 Setup Instructions

Clone or download this repository.

Open MySQL and create a new database:

create database office_db;
use office_db;


Import the SQL file:

mysql -u username -p office_db < office_db_with_triggers.sql


Run queries to test the setup.

🔍 Example Usage

Insert a new employee and check logs:

insert into employee values (110, "Kevin", "Malone","1978-02-19","M",69000,106,3);

-- View audit logs
select * from data_stamp;
select * from sex_stamp;


Expected output:

data_stamp: "Added new employee"

sex_stamp: "Added male employee"

📖 Example Queries

Some included queries:

List employees ordered by salary:

select * from employee order by salary desc;


Find all female employees born after 1970:

select count(emp_id) from employee where sex = "F" and birth_date > "1970-01-01";


Join employees with their branches:

select e.first_name, e.last_name, b.branch_name
from employee e
join branch b on e.branch_id = b.branch_id;
