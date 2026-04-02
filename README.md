# Preface 

This project is about migrating enterprise data from SQL Server into PostGres.

We'll be using 

- SQL
- Python
- Jypeter Notebook

# Pseudocode

## High-level

1. Audit the data in SQL Server (Before Migration)
2. Extract data from SQL Server (SSMS)
3. Transform the data 
4. Load data into PostgreSQL
5. Validate the data (After migration)
6. Generate a Validation report

## Low-Level

- Create a .env file
- Load env variable
- Connect to SQL Server (pyodbc)
- Connect to Postgres (psycopg2)
- Audit the data
- For each table: 
    - Get row count
    - Extract all rows
    - Transform the colomn names to lowercase
    - Convert the data types
    - Create tables in Postgres
    - Load tables into Postgres
- Run post-data migration checks
- Generate validation report