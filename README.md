# 🎓 Student Data Entry Application

This is a simple **Student Data Entry** Java application that connects to a **MySQL database using JDBC**. It supports all basic **CRUD operations**: Create, Read, Update, and Delete student records.

---

## ✨ Features

- ➕ **Add Student** – Add a new student with PRN, name, and age  
- 📋 **Display All Students** – View all student records from the database  
- 🔍 **Search Student** – Find students by PRN, name, or ID  
- ✏️ **Update Student** – Modify student name and age using PRN  
- ❌ **Delete Student** – Remove a student record using PRN  

---

## 🛠️ Requirements

- Java (JDK 8 or later)  
- MySQL Server (running locally or remotely)  
- MySQL Connector/J (JDBC driver)  
- IntelliJ IDEA (or any Java IDE)

---

## ⚙️ Setup Instructions

### 1️⃣ Create Database & Table

```sql
CREATE DATABASE student_db;

USE student_db;

CREATE TABLE students (
    id INT AUTO_INCREMENT PRIMARY KEY,
    prn VARCHAR(20) NOT NULL UNIQUE,
    name VARCHAR(100) NOT NULL,
    age INT NOT NULL
);
2️⃣ Add MySQL JDBC Driver to IntelliJ
Download the MySQL JDBC driver from MySQL Downloads

In IntelliJ:

Go to File > Project Structure > Modules > Dependencies

Click + > JARs or directories

Select the downloaded .jar file

Click Apply and OK

3️⃣ Update Database Credentials
In your Main.java, update the database connection details:

java
Copy
Edit
private static final String URL = "jdbc:mysql://localhost:3306/student_db";
private static final String USER = System.getenv("DB_USER");
private static final String PASSWORD = System.getenv("DB_PASSWORD");
💡 Tip: You can also replace System.getenv(...) with your actual credentials (not recommended for production use).

4️⃣ Run the Application
Open your project in IntelliJ

Open Main.java

Right-click and select Run 'Main'

📋 Available Operations in App
➕ Add Student

📋 Display All Students

🔍 Search Student by PRN, name, or ID

✏️ Update Student details using PRN

❌ Delete Student using PRN

🚪 Exit Application

📌 Coding Highlights
Clean OOP structure with modular code

Proper exception handling using SQLException

User-friendly prompts and menu-driven system

Uses PreparedStatement to prevent SQL Injection

🧑‍💻 Author
Name: Arjun
Semester: 4
Project Type: JDBC CRUD App
GitHub: Student-Data-Entry-JDBC

📦 Built With: Java + JDBC + MySQL
🧾 PRN: [Your PRN Here]
📚 Batch: [Your Batch Name Here]
