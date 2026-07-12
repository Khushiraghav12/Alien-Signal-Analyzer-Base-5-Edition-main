# Alien-Signal-Analyzer-Base-5-Edition-main
# 🛸 Alien Signal Analyzer (Base-5 Edition)

## 📌 Project Overview

**Alien Signal Analyzer** is a Flask-based web application that solves a fictional alien communication problem. The alien signals are represented using a **base-5 numeral system**, where one digit is corrupted and shown as **'?'**.

The application determines which digit (**0–4**) should replace the missing value so that the complete base-5 number becomes **divisible by 7**. It also supports **extra spaces** and **leading zeros**, making the input more flexible and user-friendly.

---

## ✨ Features

* 🔹 Accepts a signal containing exactly one **'?'**
* 🔹 Removes unnecessary spaces from the input
* 🔹 Supports leading zeros in the signal
* 🔹 Tries every possible base-5 digit (0–4)
* 🔹 Converts the completed base-5 number to decimal
* 🔹 Checks divisibility by **7**
* 🔹 Displays step-by-step reasoning for each attempt
* 🔹 Clean and responsive web interface built with Flask, HTML, and CSS

---

## 🛠️ Technologies Used

* Python
* Flask
* HTML
* CSS

---

## 🧠 Algorithm

1. Read the input signal.
2. Remove extra spaces using `strip()` and `replace()`.
3. Verify that the signal contains exactly one `'?'`.
4. Replace `'?'` with each digit from **0 to 4**.
5. Convert the resulting base-5 number into decimal using:

   ```python
   int(candidate, 5)
   ```
6. Check whether the decimal value is divisible by **7**.
7. Return the correct digit if found; otherwise, return **-1**.

---

## 🚀 How to Run

1. Clone or download the repository.
2. Install Flask:

   ```bash
   pip install flask
   ```
3. Start the application:

   ```bash
   python app.py
   ```
4. Open your browser and visit:

   ```
   http://127.0.0.1:5000
   ```

---

## 🧪 Sample Test Cases

| Input Signal | Output              | Explanation                                             |
| ------------ | ------------------- | ------------------------------------------------------- |
| `1?34`       | `-1`                | No replacement makes the number divisible by 7          |
| `?121`       | `1`                 | 1121 (base-5) = 161, and 161 is divisible by 7          |
| `02?1`       | `1`                 | 0211 (base-5) = 56, and 56 is divisible by 7            |
| `00?21`      | Valid digit or `-1` | Extra spaces are removed and leading zeros are accepted |

---

## 📂 Project Structure

```text
Alien-Signal-Analyzer/
│── app.py
│── README.md
│
├── static/
│   └── style.css
│
└── template/
    └── index.html
```

---

## 📜 License

This project was developed for **academic and hackathon purposes**. It is free to use for learning and educational activities.
