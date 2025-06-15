# 📚 Library Management System – SQL Mini Project

This is a beginner SQL project that simulates a basic library system using structured queries. It demonstrates database design, DDL and DML commands, and SQL constraints.

---

## 🗂️ Database Tables

### 📘 Books
Stores book details.
- `book_id` (Primary Key)
- `title`
- `author`
- `published_year`
- `genre`

### 👤 Members
Stores library member info.
- `member_id` (Primary Key)
- `name`
- `email` (Unique)
- `join_date` (Auto-generated timestamp)

### 🔁 BorrowedBooks
Tracks borrow/return activities.
- `borrow_id` (Primary Key)
- `member_id` (FK)
- `book_id` (FK)
- `borrow_date` (Auto-timestamp)
- `return_date`

---

## 🔧 Technologies Used
- SQL (MySQL Compatible)
- Online IDE: [IDGroom](https://idgroom.com/)  
- GitHub for version control and showcasing

---

## 🧪 What I Practiced
- `CREATE`, `INSERT`, `UPDATE`, `DELETE`
- `PRIMARY KEY`, `UNIQUE`, `NOT NULL`, `DEFAULT CURRENT_TIMESTAMP`
- Table relationships using `FOREIGN KEY`

---

## 💡 How to Run
1. Use any online SQL runner (e.g., [db-fiddle](https://www.db-fiddle.com/), [sqliteonline.com](https://sqliteonline.com))
2. Copy and paste the `library_management.sql` code
3. Run and experiment

---

## 🧑‍💻 Author
**Saurabh Saini**  
Finance Professional | Learning SQL & Data Analytics  
🔗 [LinkedIn Profile]([https://www.linkedin.com/in/saurabhsaini/](https://www.linkedin.com/in/saurabh-saini-4505b2b8/))
