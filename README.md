# ⚽ Football Ticket Booking System

This project is a PostgreSQL database design assignment for a **Football Ticket Booking System**. It demonstrates database design, table relationships, and SQL query implementation.

---

## 📌 Project Overview

The system manages:

- Users (Football Fans & Ticket Managers)
- Football Matches
- Ticket Bookings

It also demonstrates:

- Database schema design
- Primary Key & Foreign Key relationships
- SQL queries using filtering, joins, subqueries, aggregation, null handling, and pagination.

---

## 🛠️ Technologies Used

- PostgreSQL
- SQL
- Draw.io / Lucidchart (ERD)

---

## 📂 Database Tables

### 1. Users

Stores registered users of the system.

| Column       | Description                   |
| ------------ | ----------------------------- |
| user_id      | Primary Key                   |
| full_name    | User's full name              |
| email        | Unique email address          |
| role         | Ticket Manager / Football Fan |
| phone_number | Contact number                |

---

### 2. Matches

Stores football match information.

| Column              | Description        |
| ------------------- | ------------------ |
| match_id            | Primary Key        |
| fixture             | Match teams        |
| tournament_category | Tournament name    |
| base_ticket_price   | Ticket price       |
| match_status        | Match availability |

---

### 3. Bookings

Stores ticket booking information.

| Column         | Description           |
| -------------- | --------------------- |
| booking_id     | Primary Key           |
| user_id        | Foreign Key → Users   |
| match_id       | Foreign Key → Matches |
| seat_number    | Reserved seat         |
| payment_status | Payment status        |
| total_cost     | Total booking amount  |

---

## 🔗 Database Relationships

- One User → Many Bookings
- One Match → Many Bookings
- Each Booking belongs to one User and one Match

---

## 📁 Project Structure

```
football-ticket-booking-system/
│
├── README.md
├── schema.sql
├── insert_data.sql
├── QUERY.sql
└── ERD.png (optional)
```

---

## 📜 SQL Queries Included

The project includes the following SQL queries:

1. Retrieve available Champions League matches.
2. Search users using `ILIKE`.
3. Handle NULL values using `COALESCE`.
4. Retrieve booking details using `INNER JOIN`.
5. Display all users with bookings using `LEFT JOIN`.
6. Find bookings above the average ticket price using a subquery.
7. Retrieve the top expensive matches using `ORDER BY`, `LIMIT`, and `OFFSET`.

---

## ▶️ How to Run

1. Create a PostgreSQL database.
2. Execute `schema.sql`.
3. Execute `insert_data.sql`.
4. Run the queries from `QUERY.sql`.

---

## 📊 ERD

ERD Link:

> **Paste your Draw.io or Lucidchart public link here**

Example:

```
https://drawsql.app/teams/md-saddam/diagrams/football-ticket-booking-system

```

---

## 👨‍💻 Author

**Md Saddam Hossain**

GitHub:
https://github.com/Saddam2508/b7-a03-booking-system
