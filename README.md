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

