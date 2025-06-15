# 📚 Library Management System – SQL Mini Project

This is a beginner SQL project that simulates a basic library system using structured queries. It demonstrates database design, DDL and DML commands, and SQL constraints.

---

## 🗂️ Database Tables

### 📘 Books
Stores details of books available in the library.
- `book_id` INT (Primary Key)
- `title` VARCHAR
- `author` VARCHAR
- `published_year` INT
- `genre` VARCHAR

### 👤 Members
Stores information about registered members.
- `member_id` INT (Primary Key)
- `name` VARCHAR
- `email` VARCHAR (Unique)
- `join_date` TIMESTAMP (Default: current timestamp)

### 🔁 BorrowedBooks
Tracks which members borrowed which books and when.
- `borrow_id` INT (Primary Key)
- `member_id` INT (Foreign Key)
- `book_id` INT (Foreign Key)
- `borrow_date` TIMESTAMP (Default: current timestamp)
- `return_date` DATE

---

## 🔧 Technologies Used
- SQL (MySQL Compatible)
- Online IDE: [IDGroom](https://idgroom.com/)  
- GitHub for version control and showcasing

---

## 🧪 What I Practiced

- `CREATE TABLE`, `INSERT INTO`, `UPDATE`, `DELETE`
- `PRIMARY KEY`, `UNIQUE`, `NOT NULL`
- `DEFAULT CURRENT_TIMESTAMP`
- `FOREIGN KEY` relationships

---

## 💡 How to Run
1. Use any online SQL runner (e.g., [db-fiddle](https://www.db-fiddle.com/),
2. [sqliteonline.com](https://sqliteonline.com))
3. Copy and paste the `library_management.sql` code
4. Run and experiment

---

## 🧑‍💻 Author
**Saurabh Saini**  
Finance Professional | Learning SQL & Data Analytics  
🔗 [LinkedIn Profile]([https://www.linkedin.com/in/saurabhsaini/](https://www.linkedin.com/in/saurabh-saini-4505b2b8/))
