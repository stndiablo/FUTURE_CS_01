# DVWA Vulnerability Testing 

This repository documents the three major web vulnerabilities exploited using Damn Vulnerable Web Application (DVWA) as part of my cybersecurity internship assignment. The DVWA instance was hosted locally using XAMPP, and Burp Suite was used to intercept and manipulate HTTP requests.

---

## 🔐 Credentials Used

- **Username**: `admin`
- **Password**: `password`

---

## 1. SQL Injection (Low Security)

### ✅ Goal:
Exploit an SQL Injection flaw to extract data from the database.

### 🛠 Method:
- Navigated to **DVWA > SQL Injection**.
- Entered payload: `' OR '1'='1` into the input field.
- Burp Suite was used to intercept and send the request to **Repeater**.
- Retrieved user information from the database.

### 📸 Screenshots:
- `screenshots/sqli.png`
- `screenshots/sqli_request.png`
- `screenshots/sqli_result.png`

---

## 2. Cross-Site Scripting (XSS - Stored)

### ✅ Goal:
Trigger a JavaScript alert on a victim's browser.

### 🛠 Method:
- Navigated to **DVWA > XSS (Stored)**.
- Entered payload: `<script>alert('XSS')</script>` in the comment box.
- After submission, the alert popped up, confirming execution.

### 📸 Screenshots:
- `screenshots/xss_reflect.png`
- `screenshots/xss_stored.png`

---

## 3. Authentication Bypass

### ✅ Goal:
Login as an authorized user without knowing the correct password.

### 🛠 Method:
- Used Burp Suite to intercept login POST request.
- Modified the request to bypass validation logic.
- Successfully logged in with:
  - **Username**: `'`
  - **Password**: `anything`

### 📸 Screenshots:
- `screenshots/auth_bypass_dvwa.png`
- `screenshots/auth_bypass_request.png`
- `screenshots/auth_bypass_login.png`

---

#
