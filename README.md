# 📊 Netflix Data Analysis with MySQL

This project is a comprehensive SQL analysis of the Netflix Titles dataset using MySQL 8.0. It demonstrates practical applications of core SQL concepts including data filtering, aggregation, joining, and optimization techniques like indexing and views.

---

## 🔧 Technologies Used

- MySQL 8.0 (Command Line Client)
- Netflix Titles Dataset (CSV)
- SQL (DDL + DML + Views + Indexes)

---

## 📂 Features & Queries Covered

### 🔹 Basic Queries
- `SELECT`, `WHERE`, `ORDER BY`, `GROUP BY`
- Filter titles by type, year, country, etc.

### 🔹 Intermediate Techniques
- Aggregate functions: `SUM`, `AVG`, `COUNT`
- Subqueries for top countries, genres
- JOINS with a manually created `genres` table

### 🔹 Advanced Optimization
- Created Views (`recent_movies`)
- Indexing for fast filtering (`country`, `release_year`)
- `EXPLAIN` to analyze query performance

---

## 📁 Sample Outputs

**Recent Movies View**
```sql
CREATE VIEW recent_movies AS
SELECT title, release_year
FROM netflix_titles
WHERE type = 'Movie' AND release_year >= 2020;
