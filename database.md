# 🗄️ Database Management & SQL — Expanded Crash Guide

> Use this as a quick review map before interviews.
> Try to explain each topic in **60–90 seconds**.

---

# 📚 Core Goal

* Understand relational database concepts
* Explain keys and relationships
* Detect simple SQL mistakes
* Understand common SQL operations and constraints

### Most Common Interview Questions

* Primary keys & foreign keys
* Database integrity
* Relationship types
* SQL query debugging
* Joins
* GROUP BY & HAVING
* Normalization
* Transactions & ACID
* DELETE vs DROP vs TRUNCATE

---

# 🧱 Relational Model

A relational database stores data in **tables**.

* Rows → records
* Columns → attributes

Example:

| student_id | name  | age |
| ---------- | ----- | --- |
| 1          | Alice | 22  |

## ✅ Interview Answer

> A relational database organizes data into tables and uses keys to connect related data.


---

# 🔑 Primary Key

A primary key uniquely identifies each row in a table.

### Rules

* Must be unique
* Cannot be NULL

Example:

* `student_id`

## ✅ Interview Answer

> A primary key is the unique identifier of a record, such as student_id in a students table.


---

# 🔗 Foreign Key

A foreign key references the primary key of another table.

It creates relationships between tables and supports **referential integrity**.

## Example

### Students Table

| student_id | name  |
| ---------- | ----- |
| 1          | Alice |

### Orders Table

| order_id | student_id |
| -------- | ---------- |
| 10       | 1          |

`student_id` inside `orders` is a foreign key.

## ✅ Interview Answer

> A foreign key connects two tables and ensures that references point to valid records.



---

# 🛡️ Database Integrity

Database integrity means data remains:

* Accurate
* Valid
* Consistent

## Main Types

| Type                  | Purpose               |
| --------------------- | --------------------- |
| Entity Integrity      | Protects primary keys |
| Referential Integrity | Protects foreign keys |
| Domain Integrity      | Ensures valid values  |

## ✅ Interview Answer

> Integrity constraints prevent inconsistent data, such as an order pointing to a user that does not exist.


---

# 🔄 Relationship Types

## One-to-One (1:1)

One record relates to one record.

Example:

* User ↔ Passport

---

## One-to-Many (1:N)

One record relates to many records.

Example:

* User ↔ Orders

---

## Many-to-Many (M:N)

Many records relate to many records.

Example:

* Students ↔ Courses

Usually implemented using a **junction table**.

Example:

* `student_courses`

## ✅ Interview Answer

> A student-course relationship is many-to-many and is usually stored using a student_courses table.



---

# 🔍 SQL SELECT & WHERE

## Basic Structure

```sql
SELECT name
FROM students
WHERE age > 20;
```

### Important Concept

* `WHERE` filters rows **before** grouping
* `WHERE` cannot directly filter aggregate results after `GROUP BY`

## ✅ Interview Answer

> WHERE filters individual rows before aggregation.

## 🔍 YouTube Search Keywords

`SQL SELECT WHERE basics`

---

# 🔗 SQL Joins

Joins combine data from multiple related tables.

---

## INNER JOIN

Returns only matching rows.

```sql
SELECT users.name, orders.id
FROM users
INNER JOIN orders
ON users.id = orders.user_id;
```

---

## LEFT JOIN

Returns:

* All rows from left table
* Matching rows from right table

If no match exists → NULL values appear.

## ✅ Interview Answer

> A join is used when data is split across related tables, such as users and orders.


---

# 📊 GROUP BY & HAVING

`GROUP BY` creates groups.

Aggregate functions summarize each group:

* COUNT
* SUM
* AVG
* MIN
* MAX

---

## WHERE vs HAVING

| Clause | Works On              |
| ------ | --------------------- |
| WHERE  | Rows before grouping  |
| HAVING | Groups after grouping |

---

## Example

```sql
SELECT department, COUNT(*)
FROM employees
GROUP BY department
HAVING COUNT(*) > 5;
```

## ✅ Interview Answer

> Use WHERE before grouping and HAVING after grouping, especially with COUNT, SUM, AVG, MIN, or MAX.

## 🔍 YouTube Search Keywords

`SQL group by having difference`

---

# 🧹 Normalization

Normalization reduces:

* Data redundancy
* Update anomalies
* Inconsistent data

---

## Normal Forms

| Form | Purpose                      |
| ---- | ---------------------------- |
| 1NF  | Remove repeating groups      |
| 2NF  | Remove partial dependency    |
| 3NF  | Remove transitive dependency |

## ✅ Interview Answer

> Normalization helps avoid duplicated and inconsistent data.


---

# 💳 Transactions & ACID

A transaction is a group of database operations treated as one unit.

## ACID Properties

| Property    | Meaning                       |
| ----------- | ----------------------------- |
| Atomicity   | All or nothing                |
| Consistency | Data remains valid            |
| Isolation   | Transactions do not interfere |
| Durability  | Saved changes survive crashes |

---

## Example

Bank transfer:

* Money removed from one account
* Money added to another

Either both succeed or neither happens.

## ✅ Interview Answer

> A bank transfer should be a transaction: either both debit and credit happen, or neither happens.

## 🔍 YouTube Search Keywords

`database transactions ACID`

---

# ⚡ Indexes

An index improves search speed in a database.

Usually used on columns in:

* WHERE
* JOIN
* ORDER BY

---

## Trade-Off

### Advantages

* Faster reads
* Faster filtering

### Disadvantages

* More storage
* Slower INSERT/UPDATE

## ✅ Interview Answer

> An index improves read performance, but too many indexes can slow down insert and update operations.



---

# ❌ DELETE vs TRUNCATE vs DROP

Understanding the difference is a very common interview question.

| Command  | Removes       | WHERE Allowed | Keeps Table |
| -------- | ------------- | ------------- | ----------- |
| DELETE   | Selected rows | ✅ Yes         | ✅ Yes       |
| TRUNCATE | All rows      | ❌ No          | ✅ Yes       |
| DROP     | Entire table  | ❌ No          | ❌ No        |

---

## Examples

### DELETE

```sql
DELETE FROM users
WHERE age < 18;
```

---

### TRUNCATE

```sql
TRUNCATE TABLE users;
```

---

### DROP

```sql
DROP TABLE users;
```

## ✅ Interview Answer

> DELETE is for rows, TRUNCATE is for all rows, and DROP is for the table itself.

---

# 🎯 Final Interview Tips

* Explain concepts with small examples
* Always mention relationships between tables
* Know the difference between WHERE and HAVING
* Practice reading SQL queries aloud
* Mention performance considerations when discussing indexes or joins

---

# ⚡ Quick Revision Checklist

* [ ] Relational Model
* [ ] Primary Keys
* [ ] Foreign Keys
* [ ] Database Integrity
* [ ] Relationship Types
* [ ] SELECT & WHERE
* [ ] INNER JOIN vs LEFT JOIN
* [ ] GROUP BY & HAVING
* [ ] Normalization
* [ ] Transactions & ACID
* [ ] Indexes
* [ ] DELETE vs TRUNCATE vs DROP

---

Good luck with your interview 🚀
