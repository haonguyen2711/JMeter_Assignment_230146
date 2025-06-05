
<h1 align="center">📊 JMeter Web Performance Testing Assignment</h1>
<h3 align="center">MSSV: 230146 | Website: <a href="https://vnexpress.net">VnExpress.net</a></h3>

<p align="center">
  <img src="https://img.shields.io/badge/JMeter-5.6.3-blue" alt="JMeter Version" />
  <img src="https://img.shields.io/badge/Tested%20With-vnexpress.net-brightgreen" />
  <img src="https://img.shields.io/badge/StudentID-230146-blueviolet" />
</p>

---

## 🧠 Overview

This project demonstrates performance testing using **Apache JMeter** for the website [vnexpress.net](https://vnexpress.net), based on a student ID rule:

> MSSV ends with `46` → use `https://vnexpress.net`

## 🔧 Environment Setup

Make sure you have:

- ✅ Java JDK 17+
- ✅ Apache JMeter [Download here](https://jmeter.apache.org/download_jmeter.cgi)
- ✅ Git (optional, for source control)

---

## 🧪 Test Plan Description

### 🧵 Thread Group 1 – Basic Test

| Property         | Value            |
|------------------|------------------|
| Threads (users)  | 16 (`10 + 230146 % 10`) |
| Loop Count       | 5                |
| Request Type     | HTTP GET         |
| Target           | Homepage         |

---

### 💥 Thread Group 2 – Heavy Load Test

| Property         | Value                      |
|------------------|----------------------------|
| Threads (users)  | 66 (`50 + 230146 % 20`)    |
| Ramp-Up Time     | 30 seconds                 |
| Request Type     | HTTP GET (homepage + subpage) |
| Target Pages     | `/` and `/khoa-hoc-cong-nghe` |

---

### 🎯 Thread Group 3 – Custom Scenario

| Property         | Value                      |
|------------------|----------------------------|
| Threads (users)  | 26 (`20 + 230146 % 15`)    |
| Duration         | 60 seconds                 |
| Request Type     | HTTP GET (x2 pages)        |
| Target Pages     | `/khoa-hoc-cong-nghe`, `/suc-khoe` (custom) |

---

## ⚙️ Variables & Parameters

- User Defined Variable:
  ```text
  StudentID = 230146
  ```
- Used in query string:
  ```
  ?student_id=${StudentID}
  ```

---

## 📈 Sample Results (View with JMeter's "Summary Report")

- Average Response Time
- Throughput (requests/sec)
- Error % per scenario

📸 Screenshots or CSVs are included for each Thread Group.

---



## 👨‍🎓 About Me

> 🔐 I’m studying **Cybersecurity** and exploring testing tools like JMeter, Postman, and Java for automation.

<p align="left">
  <a href="https://github.com/haonguyen2711">
    <img src="https://img.shields.io/badge/GitHub-HyanDino-blue?logo=github" />
  </a>
  <a href="https://ecard-singleid.cmc-u.edu.vn/uuid/SV_46a97e41-f177-416c-a2b1-18ba2af20710">
    <img src="https://img.shields.io/badge/CMC%20University-Student-blueviolet" />
  </a>
</p>

---

## 📌 License

This project is for educational purposes only. Feel free to fork and study!
