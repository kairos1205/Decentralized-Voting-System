# 🗳️ Decentralized Voting System Using Ethereum Blockchain

A secure, transparent, and trustless voting platform built on the **Ethereum blockchain**. This project leverages **smart contracts**, **JWT-based authentication**, and a clean frontend interface to demonstrate how decentralized technologies can modernize electoral systems.

> ⚠️ **Note:** This project is no longer actively maintained.

---

## 🔍 Overview

This decentralized voting system enables remote, anonymous, and tamper-proof elections. Votes are recorded on the Ethereum blockchain, ensuring full transparency and eliminating centralized points of failure.

🧠 Built for learning and demonstration purposes, this project is ideal for those exploring how blockchain can be applied in real-world governance scenarios.

🎥 **Live Demo**: [Watch on YouTube](https://www.youtube.com/watch?v=bu-lWjeBtIE)

---

## ✨ Features

* 🔐 **JWT Authentication** – Secure voter login and role-based access control.
* ⛓️ **Ethereum Integration** – Votes are recorded on-chain for full transparency.
* 🤝 **Trustless Process** – No central authority; smart contracts manage logic.
* 📊 **Admin Panel** – Add candidates, set election periods, and view results.
* 🖥️ **User-Friendly UI** – Easy-to-use interface for voters and admins alike.

---

## 🛠️ Tech Stack & Requirements

### Backend

* **FastAPI** (Python 3.9)
* **MySQL** (Port: 3306)
* **JWT Authentication**
* **Uvicorn**

### Frontend

* **Node.js** (v18.14.0)
* **Browserify**
* **HTML/CSS/JS**

### Blockchain

* **Truffle**
* **Ganache**
* **Metamask**
* **Solidity (Smart Contracts)**

---

## 📸 Screenshots

| Admin Panel                                                                          | Candidate View                                                                       | Voting Interface                                                                     |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| ![](https://github.com/user-attachments/assets/60660b4e-112b-4999-9032-07c4df319411) | ![](https://github.com/user-attachments/assets/3c444587-5b62-415c-8de6-039a79e1197c) | ![](https://github.com/user-attachments/assets/fa8d8b42-847f-44b6-aea0-5e064cfbcf7e) |

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/kairos1205/Decentralized-Voting-System-Using-Ethereum-Blockchain.git
```

### 2. Set Up Ganache

* Download [Ganache](https://trufflesuite.com/ganache/)
* Create a workspace named **development**
* Add `truffle-config.js` to the Truffle projects section

### 3. Set Up Metamask

* Install the [Metamask extension](https://metamask.io/download/)
* Create/import wallet and connect to Ganache:

  * **Network Name**: Localhost 7575
  * **RPC URL**: [http://localhost:7545](http://localhost:7545)
  * **Chain ID**: 1337
  * **Currency Symbol**: ETH

### 4. Set Up MySQL

* Create a new database: `voter_db`
* Create the `voters` table using:

```sql
CREATE TABLE voters (
  voter_id VARCHAR(36) PRIMARY KEY NOT NULL,
  role ENUM('admin', 'user') NOT NULL,
  password VARCHAR(255) NOT NULL
);
```

> 💡 **Tip:** Manually insert some user records to begin testing.

---

## ⚙️ Installation Steps

### Install Global Dependencies

```bash
npm install -g truffle
```

### Install Node Modules

```bash
npm install
```

### Install Python Dependencies

```bash
pip install fastapi mysql-connector-python pydantic python-dotenv uvicorn uvicorn[standard] PyJWT
```

---

## 🧪 Running the Project

> 🔧 Before running, make sure to update DB credentials in:
> `./Database_API/.env`

### 1. Compile Smart Contracts

```bash
truffle console
compile
.exit
```

### 2. Bundle JS Files

```bash
browserify ./src/js/app.js -o ./src/dist/app.bundle.js
```

### 3. Start the Node Server

```bash
node index.js
```

### 4. Start the Python API

```bash
cd Database_API
uvicorn main:app --reload --host 127.0.0.1
```

### 5. Deploy Smart Contracts

```bash
truffle migrate
```

✅ Visit the app at: [http://localhost:8080](http://localhost:8080)

🎥 Need help setting it up? Watch the full walkthrough:
[YouTube Setup Guide](https://www.youtube.com/watch?v=a5CJ70D2P-E)

---

## 🧾 Project Structure

```
├── build/                   # Compiled contracts
├── contracts/               # Solidity smart contracts
├── Database_API/            # FastAPI backend
├── migrations/              # Truffle migration scripts
├── public/                  # Favicon and other static assets
├── src/                     # Frontend assets (HTML, CSS, JS)
├── index.js                 # Node.js entry point
├── package.json             # Node project config
├── truffle-config.js        # Truffle settings
└── README.md                # Project documentation
```

---

## 📄 License

This project is licensed under the **MIT License**.
You're free to use, modify, and distribute it, as long as you retain the original license and attribution.

🔗 [View LICENSE](https://github.com/kairos1205/Decentralized-Voting-System-Using-Ethereum-Blockchain/blob/main/LICENSE)

---

## 🌟 Support

If you found this project helpful, please consider giving it a ⭐.
Your support is appreciated!
