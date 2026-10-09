# 🎓 Student Database

A PostgreSQL-based student database project built as part of the **freeCodeCamp Relational Database**.

The project demonstrates relational database design, SQL queries, Bash scripting, PostgreSQL `psql` commands, and data processing through shell scripts.

---

## 📌 Project Overview

The **Student Database** stores and manages information about:

* Students
* Courses
* Majors
* Courses taken by students
* Student GPAs
* Course and major relationships

The project uses PostgreSQL as the database system and Bash scripts to interact with and retrieve information from the database.

---

## 🛠️ Technologies Used

* **PostgreSQL** — Relational database
* **SQL** — Database queries and data manipulation
* **Bash** — Automation and command-line scripting
* **psql** — PostgreSQL command-line interface
* **Git & GitHub** — Version control

---

## 📂 Project Structure

```text
Student-Database/
│
├── students.sql
├── student_info.sh
├── courses.csv
├── students.csv
├── insert_data.sh
└── README.md
```

### `students.sql`

Contains the PostgreSQL database structure and SQL operations used to create and populate the Student Database.

### `student_info.sh`

A Bash script that connects to PostgreSQL and retrieves student information based on a student's ID.

### `courses.csv`

Contains course-related data used to populate the database.

### `students.csv`

Contains student-related data used during database population.

### `insert_data.sh`

A Bash script used to insert CSV data into the PostgreSQL database.

---

## 🗄️ Database Structure

The database contains relational tables representing the major entities in the system.

```text
                 ┌──────────────┐
                 │    majors    │
                 └──────┬───────┘
                        │
                        │ major_id
                        ▼
                 ┌──────────────┐
                 │   students   │
                 └──────┬───────┘
                        │
                        │ student_id
                        ▼
              ┌─────────────────────┐
              │   student_courses   │
              └──────────┬──────────┘
                         │
                         │ course_id
                         ▼
                  ┌──────────────┐
                  │   courses    │
                  └──────────────┘
```

The relationships between these tables allow student, major, and course information to be queried efficiently.

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/RootPhantom/Student-Database.git
cd Student-Database
```

### 2. Start PostgreSQL

Make sure PostgreSQL is installed and running on your system.

Check the PostgreSQL version:

```bash
psql --version
```

### 3. Create the database

```bash
createdb students
```

### 4. Load the database

Run:

```bash
psql -d students -f students.sql
```

### 5. Run the student information script

Make the script executable:

```bash
chmod +x student_info.sh
```

Then run:

```bash
./student_info.sh <student_id>
```

Example:

```bash
./student_info.sh 1
```

---

## 🔍 SQL Concepts Practiced

This project helped practice several important PostgreSQL concepts:

* `CREATE DATABASE`
* `CREATE TABLE`
* Primary keys
* Foreign keys
* Constraints
* `INSERT`
* `SELECT`
* `UPDATE`
* `DELETE`
* `WHERE`
* `ORDER BY`
* `GROUP BY`
* `HAVING`
* Aggregate functions
* `JOIN`
* `LEFT JOIN`
* `FULL JOIN`
* `DISTINCT`
* Pattern matching
* Case-insensitive searches with `ILIKE`

---

## 🐚 Bash Concepts Practiced

The project also uses Bash scripting concepts such as:

* Command-line arguments
* Variables
* Conditional statements
* PostgreSQL `psql` commands
* Query execution from Bash
* Formatted output
* Database interaction through shell scripts

---

## 📚 What I Learned

Through this project, I practiced:

* Designing relational databases
* Creating relationships between tables
* Writing complex SQL queries
* Working with PostgreSQL
* Using joins and aggregate functions
* Automating database operations with Bash
* Connecting shell scripts with PostgreSQL
* Managing a project with Git and GitHub

---

## 🏷️ Project Progress

The repository uses Git tags to track certification progress:

| Tag      | Progress                  |
| -------- | ------------------------- |
| `part-1` | Student Database — Part 1 |
| `part-2` | Student Database — Part 2 |

---

## 👨‍💻 Author

**Anurag Singh**

B.Tech Computer Science & Engineering

GitHub: **[@RootPhantom](https://github.com/RootPhantom)**

---

## 📜 Certification

This project is part of the **freeCodeCamp Relational Database Certification** curriculum.

---

⭐ If you found this project useful, consider starring the repository.
