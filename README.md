# 📚 Library Management System – Java (Easy Explanation)

## 1. Project Overview
This is a **Library Management System** built using **Java**.  
It is mainly designed to understand **Object-Oriented Programming (OOP)** and **Object-Oriented Analysis & Design (OOAD)** concepts.

The system works on a **console-based interface** (text-based, no graphics) and uses a **database** to store information like books, users, and issued records.

The goal of this project is to manage:
- Books in a library  
- Users (borrowers, clerks, librarians, admin)  
- Book issuing, returning, and fines  

---

## 2. Technologies Used
- **Java (JDK 8)** – Main programming language  
- **VS Code IDE** – To run and manage the project  
- **Java DB (Derby)** – Database to store library data  
- **OOP Concepts** – Classes, objects, inheritance, abstraction, etc.

---

## 3. Key Design Idea (In Simple Words)
- Each real-life thing is represented as a **class**  
  - Example: Book, Borrower, Librarian  
- Each class has:
  - **Data** (variables)  
  - **Actions** (methods)  
- Database handles permanent storage  
- Code is written in a **clean and separated way**, so changes are easy

---

## 4. Main Users (Actors)
The system has **4 types of users**:

### 1. Borrower
A normal library member who borrows books.

### 2. Checkout Clerk
Handles book issuing and returning.

### 3. Librarian
Manages books in the library.

### 4. Administrator
Controls staff and views reports.

---

## 5. What Each User Can Do (Use Cases)

### 👤 Borrower
- Search books by:
  - Title  
  - Author  
  - Subject  
- Place a **hold request** if a book is already issued  
- View:
  - Personal details  
  - List of borrowed books  

---

### 🧾 Checkout Clerk
(All Borrower features + extra)

- Issue a book to a borrower  
- Accept returned books  
- Renew issued books  
- Record fine payment  
- Add new borrowers  
- Update borrower details (address, phone, etc.)

---

### 📚 Librarian
(All Borrower + Checkout Clerk features + extra)

- Add new books  
- Remove books  
- Update book information  

---

### 🛠️ Administrator
- Add new Clerks  
- Add new Librarians  
- View issued books history  
- View all books in the library  

---

## 6. Important Classes (Simple Explanation)

- **Book**  
  Stores book details like title, author, subject, status  

- **Borrower**  
  Stores borrower details and borrowed books  

- **HoldRequest**  
  Handles requests when a book is not available  

- **HoldRequestOperations**  
  Acts as a middle layer between Book and HoldRequest  
  (Used to reduce dependency and make code cleaner)

- **Librarian / Clerk / Admin**  
  Different user roles with different permissions  

- **Database Classes**  
  Handle saving and fetching data from the database  

---

## 7. Database
- Database name: **LMS**
- Stores:
  - Books  
  - Users  
  - Issued records  
  - Fine details 

---

## 8. How the System Works (Flow)
1. User logs in  
2. System checks user role  
3. Menu is shown based on role  
4. User selects an option  
5. Action is performed  
6. Database is updated 
