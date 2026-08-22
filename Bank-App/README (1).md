<div align="center">

# 🏦 CoreBank

### Console-based Core Banking System in Pure Java

*Accounts • Deposits • Withdrawals • Fund Transfers • Statements • Custom Exceptions*

![Java](https://img.shields.io/badge/Java-17%2B-orange)
![Type](https://img.shields.io/badge/Type-Console%20Application-green)
![Database](https://img.shields.io/badge/Database-In--Memory-blue)
![License](https://img.shields.io/badge/License-MIT-yellow)

</div>

---

## 📌 Overview

**CoreBank** is a menu-driven, console-based banking application built with **pure Java** — no frameworks, no database. It implements real-world core banking operations and demonstrates how solid fundamentals (OOP, Collections, Exception Handling) combine with clean architecture (Repository Pattern, Service Layer) to solve practical business problems.

## ✨ Features

| Feature | Description |
|---|---|
| 🆕 Account Management | Open and close customer accounts |
| 💰 Deposit | Add funds with full input validation |
| 💸 Withdrawal | Withdraw with insufficient-balance protection |
| 🔁 Fund Transfer | Move money between accounts atomically |
| 🧾 Statements | Full transaction history per account |
| 🔍 Search & Filter | Look up accounts quickly from in-memory storage |
| 🛡️ Custom Exceptions | Domain-specific errors (e.g. `InsufficientBalanceException`, `AccountNotFoundException`) |
| ✅ Validation | Robust handling of edge cases and invalid input |

## 🏗️ Architecture

The project follows **Separation of Concerns** with three clean layers:

```
┌─────────────────────────────────────┐
│   Console UI (Scanner / Menu)       │  ← user interaction
├─────────────────────────────────────┤
│   Service Layer (Business Logic)    │  ← deposit, withdraw, transfer rules
├─────────────────────────────────────┤
│   Repository (In-Memory Store)      │  ← ArrayList / HashMap (CRUD)
└─────────────────────────────────────┘
```

- **`Account`** & **`Transaction`** model classes
- **Repository Pattern** — all data access isolated behind one component
- **Service Layer** — business rules kept independent of UI and storage
- **`LocalDateTime`** — accurate transaction timestamps

## ☕ Java Concepts Applied

- ✔️ OOP Principles — Encapsulation & Abstraction
- ✔️ Collections Framework — `ArrayList`, `HashMap`
- ✔️ Custom Exception Handling
- ✔️ Input Validation & Edge-Case Handling
- ✔️ CRUD Operations without a Database
- ✔️ Design Patterns — Repository, Layered Architecture

## 🚀 Getting Started

### Prerequisites
- **JDK 17 or higher** — [download here](https://adoptium.net/) if you don't have it
- Verify your installation:
  ```bash
  java -version
  ```

### Option 1: One-click run ✅ (easiest)
1. Click **Code → Download ZIP** on this repo and extract it
2. Open the extracted folder and double-click:
   - 🪟 **Windows** → `run.bat`
   - 🍎 **macOS / Linux** → `run.sh`

That's it — the script compiles and launches CoreBank automatically.

### Option 2: Command line

```bash
# 1. Clone the repository
git clone https://github.com/zasha12/corebank.git
cd corebank

# 2. Compile all source files (bytecode goes into the out/ folder)
javac -encoding UTF-8 -d out src/corebank/*.java

# 3. Run the application
java -cp out corebank.Main
```

| Command | What it does |
|---|---|
| `javac` | Java **compiler** — turns `.java` source into `.class` bytecode |
| `-d out` | places compiled files in an `out` folder (keeps source clean) |
| `-encoding UTF-8` | safe handling of currency symbols like ₹ |
| `-cp out` | tells the JVM where to find the compiled classes |
| `corebank.Main` | the entry-point class (contains `main`) |

### Option 3: IDE (IntelliJ IDEA / Eclipse / VS Code)
Open the project folder and press ▶ **Run** on `Main.java` — no commands needed.



## 🗂️ Project Structure

```
corebank/
├── src/corebank/
│   ├── Main.java                       # Entry point + console menu
│   ├── Account.java                    # Account entity
│   ├── Transaction.java                # Transaction record
│   ├── AccountRepository.java          # In-memory CRUD store
│   ├── BankingService.java             # Deposit / withdraw / transfer logic
│   ├── InsufficientBalanceException.java
│   └── AccountNotFoundException.java
├── run.bat                             # 🪟 Windows one-click runner
├── run.sh                              # 🍎 macOS / Linux one-click runner
├── README.md
└── LICENSE
```

## 🛣️ Roadmap

- [ ] File-based persistence (save/load account data)
- [ ] Account types — Savings & Current
- [ ] Interest calculation
- [ ] Daily/monthly transaction limits
- [ ] Overdraft facility
- [ ] Move to a real database (JDBC → JPA)
- [ ] REST API with Spring Boot
- [ ] Authentication & authorization



## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

## 👤 Author

**KARTIKEYA DHASMANA**
- GitHub: [@zasha12](https://github.com/zasha12)
- LinkedIn: (https://www.linkedin.com/in/kartikeya-dhasmana-b91389245/)
- Email: kartikeyadhasmana@gmail.com

---

<div align="center">

⭐ *If you found this project helpful, consider giving it a star!*

</div>
