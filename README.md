# 🔐 PHP Authentication System

A secure and lightweight **PHP & MySQL Authentication System** featuring
user registration, login, email verification, session management, and a
protected user dashboard.

This project is ideal for:

-   Beginners learning PHP authentication\
-   Students building academic projects\
-   Developers needing a simple authentication starter template

------------------------------------------------------------------------

## 🚀 Features

-   User Registration (Sign Up)
-   User Login (Sign In)
-   Secure Password Hashing using `password_hash()`
-   Password Verification using `password_verify()`
-   Email Verification System
-   Session-Based Authentication
-   Protected Profile Page
-   SQL Injection Protection (Prepared Statements)
-   Clean & Responsive UI
-   MySQL Database Integration

------------------------------------------------------------------------

## 🛠 Tech Stack

-   PHP (Core PHP -- Procedural)
-   MySQL
-   HTML5
-   CSS3
-   JavaScript
-   Font Awesome

------------------------------------------------------------------------

## 📁 Project Structure

php-auth-main/
│
├── index.php                  # Login & Signup Page
├── profile.php                # User Dashboard (Protected)
├── verify-email.php           # Email Verification Handler
├── php-auth.sql               # Database File
├── sonar-project.properties
│
├── assets/
│   ├── style.css              # Styling
│   └── script.js              # Frontend JavaScript
│
└── include/
    ├── action.php             # Authentication Logic
    ├── constant.php           # Configuration (SITEURL)
    └── database.php           # Database Connection

------------------------------------------------------------------------

## ⚙️ Installation Guide

### 1️⃣ Clone the Repository

``` bash
git clone https://github.com/your-username/php-auth.git
```

Or download the ZIP file and extract it inside your web server
directory.

### 2️⃣ Move Project to Server Directory

If using:

-   XAMPP → `htdocs/`
-   WAMP → `www/`
-   MAMP → `htdocs/`

Example (XAMPP):

C:/xampp/htdocs/php-auth

### 3️⃣ Create Database

1.  Open **phpMyAdmin**
2.  Create a new database named:

php-auth

3.  Import the file:

php-auth.sql

### 4️⃣ Configure Database

Open:

include/database.php

Update credentials if needed:

``` php
$servername = "localhost";
$username = "root";
$password = "";
$dbname = "php-auth";
```

### 5️⃣ Set Base URL

Open:

include/constant.php

Update:

``` php
define('SITEURL', 'http://localhost/php-auth-main/php-auth-main');
```

Make sure this matches your local project folder path.

------------------------------------------------------------------------

## 🔐 Security Implementation

This project uses:

-   `password_hash()` for secure password encryption
-   `password_verify()` for login validation
-   Prepared statements (MySQLi) to prevent SQL injection
-   Session-based authentication
-   Route protection using session checks

------------------------------------------------------------------------

## 🔎 Authentication Flow

### 📝 Registration

1.  User submits signup form\
2.  Username uniqueness is checked\
3.  Password is hashed securely\
4.  User is inserted into database\
5.  Verification token is generated\
6.  Email verification required

### 🔑 Login

1.  User submits credentials\
2.  Password verified using `password_verify()`\
3.  Session created\
4.  Redirect to profile page

### 👤 Profile Page

-   Accessible only if session exists\
-   Redirects to login page if unauthorized

------------------------------------------------------------------------

## 📌 Requirements

-   PHP 7.4 or higher
-   MySQL 5.7 or higher
-   Apache / Nginx
-   Local server (XAMPP, WAMP, or MAMP)

------------------------------------------------------------------------

## 📈 Future Improvements

-   CSRF Protection
-   Password Reset System
-   Remember Me functionality
-   SMTP Email Integration
-   MVC Architecture Refactor
-   PDO Migration
-   Role-Based Access Control (RBAC)
-   API Authentication (JWT)

------------------------------------------------------------------------

## 📄 License

This project is open-source and free to use for learning and development
purposes.

------------------------------------------------------------------------

## 👨‍💻 Author

Developed as a lightweight PHP authentication starter template.

If you found this useful, feel free to ⭐ the repository.
