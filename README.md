# SIT737-2025-Prac4P: Calculator Microservice

This repository contains the source code for the **Calculator Microservice** built as part of the SIT737 Cloud Native Application Development unit (Practical 4.1P) at Deakin University.

The microservice is designed using **Node.js** and **Express.js**, with structured logging implemented via **Winston**. It offers basic arithmetic operations via RESTful endpoints and handles errors.

---

## 📌 Features

- Perform arithmetic operations: `add`, `subtract`, `multiply`, `divide`
- RESTful API using Express
- Input validation and error handling
- Logging of requests, operations, and errors using Winston
- Logs stored in `logs/error.log` and `logs/combined.log`

---

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/en/) (v14+ recommended)
- [Git](https://git-scm.com/)
- A code editor like [VS Code](https://code.visualstudio.com/)

---

### 📁 Project Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/AdeelAhmedIqbal/sit737-2025-prac4p.git
   cd sit737-2025-prac4p
   ```

2. **Install dependencies**
   ```bash
   npm install express
   npm install Winston
   ```

3. **Run the microservice**
   ```bash
   node mycal.js
   ```

   The server will start on **http://localhost:3040**

---

## 🔌 API Endpoints

Each endpoint expects two query parameters: `n1` and `n2`.

| Operation      | Endpoint     | Example                          |
|----------------|--------------|----------------------------------|
| Addition       | `/add`       | `/add?n1=5&n2=3`                 |
| Subtraction    | `/subtract`  | `/subtract?n1=10&n2=4`          |
| Multiplication | `/multiply`  | `/multiply?n1=6&n2=7`           |
| Division       | `/divide`    | `/divide?n1=15&n2=3`            |

---

## ⚠️ Error Handling

- Missing or invalid parameters return a 500 status with an error message.
- Division by zero is handled with a custom error message.
- All errors are logged in `error.log`.

---

## 📋 Logging Details

The application uses [Winston](https://github.com/winstonjs/winston) for logging:

- **Info and error logs:** saved in `combined.log`
- **Only error logs:** saved in `error.log`
- Logs are printed to the console during development


## 👨‍💻 Author

**Adeel Ahmed Iqbal**  
**Student ID: 224404186**
GitHub: [@AdeelAhmedIqbal](https://github.com/AdeelAhmedIqbal)

---
