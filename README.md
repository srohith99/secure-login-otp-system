# secure-login-otp-system
🔐 A secure PHP-based login system with OTP email verification, brute-force protection, and session-based 2FA. Designed with a cyber-themed UI for real-world authentication use. 

# 🔐 Cyber Secure OTP Login System

A full-stack secure login system built with **HTML, CSS, PHP, MySQL**, and **PHPMailer**, featuring:
- Encrypted password storage
- OTP-based email verification
- Rate-limited brute force protection
- Cyber-themed UI for real-world cybersecurity demonstration

---

## 🚀 Features

- ✅ Secure Login & Signup
- 🔐 Password Hashing (`bcrypt`)
- 📩 Email-based OTP (One Time Password)
- ⏳ Countdown-based OTP validation (2 minutes)
- 🔁 Resend OTP feature (with rate limit)
- 🔐 Brute Force Attack Protection (IP-based logging)
- 📊 Recent Login Log Display
- 🚪 Secure Logout
- 💻 Fully styled cyber-dark UI

---

## 📸 Screenshots

> Insert screenshots or GIFs here  
> Login | Signup | OTP Input | Dashboard | Resend OTP

---

## ⚙️ Tech Stack

| Layer       | Tech                         |
|-------------|------------------------------|
| Frontend    | HTML, CSS, JavaScript        |
| Backend     | PHP                          |
| Database    | MySQL                        |
| Mail System | PHPMailer + Gmail SMTP       |

---

## 🏗️ Folder Structure

CyberSecureLoginSystem/
├── login.html
├── signup.html
├── verify.html
├── login.php
├── signup.php
├── verify.php
├── resend_otp.php
├── dashboard.php
├── logout.php
├── style.css
├── PHPMailer/
└── README.md


---

## 🧠 Learning Outcomes

- Real-world implementation of **OTP-based 2FA**
- **Password security** with `password_hash()` and `verify()`
- Handling **user sessions**, rate limits, and IP logs
- Creating **user-friendly error/success flows**
- Integrating PHPMailer for email security workflows

---

## 🧪 Setup Instructions (Localhost using XAMPP)

1. 📁 Clone this repository  
   ```bash
   git clone https://github.com/srohith99/CyberSecureLoginSystem.git

  -> use XAMPP and place at C:\xampp\htdocs\CyberSecureLoginSystem
  
2.🔌 Start XAMPP (Apache + MySQL)

3.🗃️ Create MySQL Database:

  DB Name: secure_project

  Create tables:
  CREATE TABLE users (
  id INT AUTO_INCREMENT PRIMARY KEY,
  username VARCHAR(100),
  email VARCHAR(255),
  password VARCHAR(255)
);

CREATE TABLE login_logs (
  id INT AUTO_INCREMENT PRIMARY KEY,
  username VARCHAR(100),
  ip_address VARCHAR(45),
  status VARCHAR(50),
  time TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

4.✉️ Setup PHPMailer/ inside root folder
    📦 1. Install PHPMailer (Once Only)
            Download from:
              👉 [link](https://github.com/PHPMailer/PHPMailer);
        2. Extract zip and place the PHPMailer folder inside your CyberSecureLoginSystem directory.

5.🔐 Use your Gmail + App Password in all mail files:

   -> use App Passwords (if 2FA enabled): [](https://myaccount.google.com/apppasswords);
   -> Create App and name it as PHPMailer 
   -> Copy the generated password , paste into code @login.php

  find @ login.php
  $mail->Username = 'your-email@gmail.com';
  $mail->Password = 'your-app-password'; // NOT Gmail login its password geneated during app creation.
  
6.✅ Visit http://localhost/CyberSecureLoginSystem/login.html

7.Start Working on it..


🔐 For Further Security Enhancements We Can Add,
  -Google Authenticator (TOTP)

  -Device fingerprinting

  -reCAPTCHA v3

  -Login notification emails

  -Multi-device OTP logs


🧑‍💻 Author
Rohith S – CSE(IoT, Cybersecurity, and Blockchain ) - 3rd Year - @BMSCE
If any doudts regarding it , You can 
📫 Reach me via [LinkedIn](www.linkedin.com/in/rohith-s-0b845a313); or GitHub @srohith99


