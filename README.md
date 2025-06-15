# library-management-sql
A beginner SQL mini project simulating a Library Management System
-- Create Books Table
CREATE TABLE Books (
    book_id INT PRIMARY KEY,
    title VARCHAR(100) NOT NULL,
    author VARCHAR(100),
    published_year INT,
    genre VARCHAR(50)
);

-- Create Members Table
CREATE TABLE Members (
    member_id INT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(100) UNIQUE NOT NULL,
    join_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Create BorrowedBooks Table
CREATE TABLE BorrowedBooks (
    borrow_id INT PRIMARY KEY,
    member_id INT NOT NULL,
    book_id INT NOT NULL,
    borrow_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    return_date DATE,
    FOREIGN KEY (member_id) REFERENCES Members(member_id),
    FOREIGN KEY (book_id) REFERENCES Books(book_id)
);

-- Insert Sample Books
INSERT INTO Books (book_id, title, author, published_year, genre)
VALUES 
(1, '1984', 'George Orwell', 1949, 'Dystopian'),
(2, 'To Kill a Mockingbird', 'Harper Lee', 1960, 'Fiction'),
(3, 'The Great Gatsby', 'F. Scott Fitzgerald', 1925, 'Classic');

-- Insert Sample Members
INSERT INTO Members (member_id, name, email, join_date)
VALUES 
(101, 'Ravi Sharma', 'ravi@example.com', '2024-10-01'),
(102, 'Anjali Mehra', 'anjali@example.com', '2024-11-15'),
(103, 'Karan Joshi', 'karan@example.com', '2025-01-05');

-- Record Borrowed Books
INSERT INTO BorrowedBooks (borrow_id, member_id, book_id, borrow_date, return_date)
VALUES 
(1, 101, 2, '2025-05-20', NULL),
(2, 103, 1, '2025-05-22', '2025-06-01');

-- Update a book's published year
UPDATE Books
SET published_year = 1950
WHERE book_id = 1;

-- Delete a member (only if they haven’t borrowed a book)
DELETE FROM Members
WHERE member_id = 102;
