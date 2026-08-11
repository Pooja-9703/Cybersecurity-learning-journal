# E. Database SQL Basics

## 1. Database

- A database is an organised place where a computer stores information.
- Think of it as a digital notebook that allows computers to:
  - Search information quickly
  - Count records
  - Sort information
  - Retrieve specific information

---

## 2. Tables

- Information inside a database is stored in **tables**.
- A table consists of **columns** and **rows**.

---

## 3. Columns — "What information?"

A column represents **one type/category of information**.

---

## 4. Rows — "Which record?"

A row represents **one complete record**.

---

## 5. SQL — Structured Query Language

SQL is a language used to communicate with and ask questions from databases.

---

## 6. Query

- A query is a request for information from a database.
- A basic SQL query can retrieve/display information without changing the stored data.

---

## SQL Queries

### 1. View Everything in a Table

- The `*` symbol means **all columns**.
- The `FROM` keyword tells the database which table to use.

`SELECT * FROM <table_name>;`

---

### 2. SELECT Specific Columns

We can choose specific columns by listing them after `SELECT`.

`SELECT <column1>, <column2>, ... FROM <table_name>;`

---

### 3. Filtering Rows with WHERE

The `WHERE` keyword filters rows. It keeps only rows that match a condition.

`SELECT <columns> FROM <table_name> WHERE <condition>;`

#### Example

`SELECT * FROM Orders WHERE drink = 'coffee';`

---

### 4. Sorting Results with ORDER BY

`ORDER BY` is used to sort the results based on a column.

#### Ascending Order

`SELECT * FROM <table_name> ORDER BY <column>;`

#### Descending Order

`SELECT * FROM <table_name> ORDER BY <column> DESC;`

---

### 5. Combining Filtering and Sorting

Filtering and sorting can be combined in the same query.

`SELECT <columns> FROM <table_name> WHERE <condition> ORDER BY <column> <ASC/DESC>;`

---

## SQL Keyword Summary

| Keyword | Purpose |
|---|---|
| `SELECT` | Choose what data to display |
| `FROM` | Choose where the data comes from |
| `WHERE` | Filter records based on a condition |
| `ORDER BY` | Sort the results |
| `ASC` | Sort in ascending order |
| `DESC` | Sort in descending order |
| `*` | Select all columns |

---

## Important Concept

- **SELECT** → Choose what data to display.
- **FROM** → Choose the table the data comes from.
- **WHERE** → Filter the records based on a condition.
- **ORDER BY** → Sort the results.
