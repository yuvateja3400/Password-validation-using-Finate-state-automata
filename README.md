
# 🔐 Password Validation Using Automata

This project implements a **password validation system using Deterministic Finite Automata (DFA)**. The system checks whether a password meets specific complexity requirements — ensuring it includes uppercase letters, lowercase letters, digits, and special characters.

## 📚 Table of Contents

- [Abstract](#abstract)
- [Problem Statement](#problem-statement)
- [Scope & Limitations](#scope--limitations)
- [Automata Design](#automata-design)
- [Sample Test Cases](#sample-test-cases)
- [Technologies Used](#technologies-used)
- [Authors](#authors)
- [References](#references)

---

## 🧾 Abstract

Passwords are the first line of defense against unauthorized access to digital information. Weak passwords make systems vulnerable to brute force and dictionary attacks. This project focuses on creating a **finite automaton-based system** to validate whether a given password is strong by checking:

- Presence of at least one **uppercase letter**
- Presence of at least one **lowercase letter**
- Presence of at least one **digit**
- Presence of at least one **special character** from a limited set

---

## ❓ Problem Statement

The system must determine if a password includes:
- At least one uppercase letter (A-Z)
- At least one lowercase letter (a-z)
- At least one number (0-9)
- At least one special character (`@, #, $, %, &, !`)

If the password satisfies all conditions, it is marked **valid**, otherwise **invalid**.

---

## 🔍 Scope & Limitations

- Minimum password length supported: **4**
- Special characters are limited to: `@, #, $, %, &, !`
- The DFA contains **16 defined states** for transition tracking.

---

## 🧠 Automata Design

The system uses a **Deterministic Finite Automaton (DFA)** consisting of:
- **States**: `q0` to `q15`
- **Final State**: `q15`
- **Input Symbols**: Uppercase, lowercase, numbers, and selected special characters
- **Transition Table**: Maps each state to the next based on the character type encountered

### 📈 Example Transition

```
q0 + Uppercase → q2
q2 + Number → q5
...
q11 + Special Character → q15
```

A visual DFA state diagram is included in the project files.

---

## 🧪 Sample Test Cases

1. ✅ **Valid**:  
   Input: `ABcd@#123`  
   - Contains uppercase, lowercase, digits, special characters.

2. ❌ **Invalid**:  
   Input: `abcd@1234#`  
   - Missing uppercase letters.

---

## 🛠️ Technologies Used

- DFA implemented in `.jff` format using **JFLAP** tool.
- Report prepared with supporting theory from **Theory of Computation** coursework.

---

## 👨‍💻 Authors

- CH. Yuva Teja – [CSE18023]
- V. Manoj Saiprakash – [CSE18136]
- I. Yashwanth – [CSE18043]

Project submitted at **Amrita Vishwa Vidyapeetham**, Bengaluru Campus.

---

## 📖 References

- [GeeksforGeeks: Introduction to Finite Automata](https://www.geeksforgeeks.org/introduction-of-finite-automata/)
- [JavaTpoint: Deterministic Finite Automata](https://www.javatpoint.com/deterministic-finite-automata)
