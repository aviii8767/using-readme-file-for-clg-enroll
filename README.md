# using-readme-file-for-clg-enroll


## 📌 Project Overview
A console-based application built using **.NET Framework (C#)** and **MySQL** to manage college operations efficiently. The system supports multiple user roles—**Student, Teacher, Admin, and SuperAdmin**—with tailored permissions and functionalities for each role. It ensures secure user verification, structured CRUD operations, and dynamic interaction with a relational database.

---

## 🚀 Features

🔹 **Role-based Access Control**  
- Student, Teacher, Admin, and SuperAdmin workflows  
- Each role has specific permissions and functionality

🔹 **Student Module**  
- Register as a new student or log in as an existing one  
- View and update personal info  
- Enroll in available courses  
- View enrolled courses  
- Remove profile  

🔹 **Teacher Module**  
- Register or log in as teacher  
- View/update profile  
- View assigned courses  
- View enrolled students for assigned courses  
- Add student results  
- Remove profile
  
🔹 **Admin Module**  
- Secure login with Admin ID (no new registration from admin module)  
- View/update/remove Students and Teachers  
- View lists of Courses, Departments, Semesters  

🔹 **SuperAdmin Module**  
- Higher-level access  
- Register or remove Admins  
- Add/remove Departments, Courses, and Semesters  

---

## 🧑‍💻 Technologies Used

- 💻 **.NET (C#)** — Console Application  
- 🛢️ **MySQL** — Relational Database  
- 🔌 **ADO.NET** — Database Connectivity  
- 📋 **SQL** — Data Manipulation and Querying  
- 📊 **EER Diagram** — Database Structure

---

## 🗂️ Database Schema

This project uses a **relational database schema** to manage college data in a normalized and scalable structure.

### 📌 Entities & Relationships

- **Student**, **Teacher**, **Admin**, **SuperAdmin** share location data via a common `address` table.
- **Course** is linked to `Teacher`, `Semester`, and `Department`.
- **StudentCourseEnrollment** enables many-to-many relation between `Student` and `Course`.
- **Result** table stores exam scores per student per course.

### 🔄 Relationship Summary

- **One-to-Many**
  - Department → Teachers  
  - Teacher → Courses  
  - Semester → Courses  

- **Many-to-Many**
  - Student ↔ Course (via CourseEnrollment table)

---

### 🖼️ EER Diagram

![EER Diagram](EER%20for%20College%20DB.png)

> This diagram illustrates the complete database architecture including all tables, keys, and relationships.  
> File path: `/assets/EER for College DB.png`

---

## 🙌 Acknowledgements

I would like to express my sincere gratitude to Suraj Sir for his invaluable guidance and support throughout the development of this project. His mentorship helped me understand and implement key backend and database concepts effectively.
Additionally, I am currently learning how to implement Entity Framework, which I plan to integrate into future enhancements of this application.
```
