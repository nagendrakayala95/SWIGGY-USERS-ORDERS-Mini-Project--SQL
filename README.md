````markdown
# SQL CHALLENGE — SWIGGY USERS & ORDERS (Mini Project)

Welcome to the **SQL CHALLENGE — Swiggy Users & Orders (Mini Project)** 🚀  
This mini-project is designed to help you **practice core SQL concepts end-to-end** using a realistic food-delivery use case.

---

## 📌 Project Objective

Using the data provided, you will design a complete SQL project from scratch.

You will:

- ✅ Create a **database**
- ✅ Create **two related tables** (`users` and `orders`)
- ✅ Insert data **exactly as given**
- ✅ Perform SQL operations **up to `GROUP BY`**
- ✅ Practice real-world SQL skills:
  - Filtering (`WHERE`)
  - Sorting (`ORDER BY`)
  - Pattern matching (`LIKE`)
  - Aggregations (`COUNT`, `SUM`, `AVG`, `MIN`, `MAX`)
  - Grouped reporting (`GROUP BY`, `HAVING`)

This project is perfect for **beginners to early intermediates** who want to build confidence in SQL using a practical scenario.

---

## 🧱 Database & Table Design

### 1️⃣ Database

Suggested name (you can change it if you want):

```sql
CREATE DATABASE swiggy_sql_challenge;
USE swiggy_sql_challenge;
````

---

### 2️⃣ Table 1: `users`

Stores basic information about users on the Swiggy-like platform.

> ⚠️ Column names are indicative. Use the exact structure given in your data file.

**Suggested schema:**

```sql
CREATE TABLE users (
    user_id INT PRIMARY KEY,
    user_name VARCHAR(100),
    age INT,
    gender VARCHAR(10),
    city VARCHAR(100),
    signup_date DATE
);
```

---

### 3️⃣ Table 2: `orders`

Contains order details for each user.

```sql
CREATE TABLE orders (
    order_id INT PRIMARY KEY,
    user_id INT,
    restaurant VARCHAR(150),
    cuisine VARCHAR(100),
    order_amount DECIMAL(10,2),
    order_date DATE,
    payment_mode VARCHAR(20),   -- e.g., 'UPI', 'Card', 'Cash'
    city VARCHAR(100),
    FOREIGN KEY (user_id) REFERENCES users(user_id)
);
```

> 🔁 Make sure `user_id` in `orders` matches a valid `user_id` from `users`.

---

## 📂 Repository Structure

A suggested structure for this GitHub repo:

```bash
SQL-CHALLENGE-SWIGGY-USERS-ORDERS/
├── README.md                 # Project documentation (this file)
├── schema.sql                # CREATE DATABASE + CREATE TABLE scripts
├── data_insert_users.sql     # INSERT statements for users table
├── data_insert_orders.sql    # INSERT statements for orders table
└── queries/
    ├── beginner_queries.sql
    ├── intermediate_queries.sql
    └── advanced_queries.sql
```

You can adjust the structure, but keeping things modular makes it easier to follow.

---

## ⚙️ How to Use This Project

1. **Clone the repository:**

   ```bash
   git clone https://github.com/<your-username>/SQL-CHALLENGE-SWIGGY-USERS-ORDERS.git
   cd SQL-CHALLENGE-SWIGGY-USERS-ORDERS
   ```

2. **Open your SQL tool of choice:**

   * MySQL Workbench
   * PostgreSQL / pgAdmin
   * SQL Server / SSMS
   * Oracle / etc.

3. **Run the scripts in order:**

   1. `schema.sql` → creates the database and tables
   2. `data_insert_users.sql` → inserts user data
   3. `data_insert_orders.sql` → inserts order data

4. **Start solving queries** from the `queries` folder or write your own!

---

## 🧪 Practice Tasks (Suggested)

You can structure this as a challenge set for learners.

### 🟢 Level 1 – Basic SELECT & Filtering

1. Show all users from the `users` table.
2. List all orders placed in a specific city (e.g., `Hyderabad`).
3. Get all orders where `payment_mode = 'UPI'`.
4. Find users who signed up after a certain date.
5. Display all unique cities present in the `users` table.

---

### 🟡 Level 2 – Sorting, Pattern Matching & Aggregations

6. List the **top 10 highest order amounts**.
7. Show all restaurants whose name starts with `'P'`.
8. Find the **total number of orders** placed.
9. Calculate the **average order amount**.
10. Find the **minimum and maximum order amount**.

---

### 🔵 Level 3 – GROUP BY & Reporting

11. Show **total orders per city**.

12. Show **total revenue (SUM of order_amount) per city**.

13. Show **total number of orders per payment_mode**.

14. Find the **number of orders per cuisine type**.

15. For each user, show:

    * user_id
    * total number of orders
    * total amount spent

16. Show all cities where **total revenue is greater than a threshold** (use `HAVING`).

---

### 🧠 Optional: JOIN-Based Insights

Even though the focus is **up to GROUP BY**, feel free to add some `JOIN`-based questions too (if you're comfortable):

* List each user with their total order count.
* Find users who haven’t placed any order.
* Find the top 3 users by total amount spent.

---

## ✅ Learning Outcomes

By completing this mini-project, you will:

* Understand how to **design tables** for a real-world scenario.
* Get hands-on practice with:

  * `CREATE DATABASE`, `CREATE TABLE`
  * `INSERT`, `SELECT`, `WHERE`, `ORDER BY`
  * `LIKE`, pattern matching
  * Aggregations: `COUNT`, `SUM`, `AVG`, `MIN`, `MAX`
  * `GROUP BY`, `HAVING`
* Learn to **organize SQL projects** in a GitHub repository.

---

## 🤝 How to Contribute

If this is a public repo and you want others to contribute:

1. **Fork** the repository

2. Create a new branch:

   ```bash
   git checkout -b feature-new-queries
   ```

3. Commit your changes:

   ```bash
   git commit -m "Added new Swiggy queries"
   ```

4. Push the branch and open a **Pull Request**

---

## 📜 License

You can use any license you prefer (MIT is a common choice). Example:

```text
This project is licensed under the MIT License.
```

---

## 💬 Feedback / Contact

If you found this SQL challenge helpful, feel free to:

* ⭐ Star the repository on GitHub
* Share it with other learners
* Open an issue or PR with improvements

Happy Querying! 🧡🍽️
`SELECT * FROM swiggy_life;`

```
```
