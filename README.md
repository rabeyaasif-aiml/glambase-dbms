# 💄 GlamBase

**A full-stack cosmetics store management system** built with React, Flask, and MySQL — featuring a relational database backed by triggers, stored procedures, and views.

![React](https://img.shields.io/badge/Frontend-React-61DAFB?logo=react&logoColor=white)
![Flask](https://img.shields.io/badge/Backend-Flask-000000?logo=flask&logoColor=white)
![MySQL](https://img.shields.io/badge/Database-MySQL-4479A1?logo=mysql&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-success)

---

## 📖 Overview

GlamBase is a database-driven cosmetics store application that manages products, customers, orders, and inventory in one place. It started as a DBMS semester project and grew into a complete full-stack app, with business logic pushed down into the database layer (triggers, procedures, views) rather than living only in application code.

## ✨ Features

- 🛍️ Product catalog with categories and brands
- 👤 Customer management
- 🧾 Order placement and order history
- 📦 Automatic stock updates through database triggers
- 🔍 Reporting through SQL views
- ⚙️ Reusable logic through stored procedures
- 🔌 REST API connecting the React frontend to MySQL

## 🏗️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | React |
| Backend | Python, Flask |
| Database | MySQL |
| Version Control | Git, GitHub |

## 🗄️ Database Design

The database is designed around these core entities:

- `Customers`
- `Products`
- `Categories`
- `Orders`
- `Order_Items`

**Database objects used:**

- **Triggers** — e.g. reduce stock automatically when an order is placed
- **Stored Procedures** — e.g. place an order, fetch customer history
- **Views** — e.g. sales summary, low-stock products

## 🔌 Backend / API

The Flask backend exposes REST endpoints that the React frontend consumes.

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/products` | Get all products |
| POST | `/api/orders` | Place a new order |
| GET | `/api/customers` | Get all customers |

## ⚙️ How to Run

### Prerequisites

- [Node.js](https://nodejs.org/) (v16+)
- [Python](https://www.python.org/) (v3.8+)
- [MySQL](https://www.mysql.com/) Server

### 1. Clone the repository

```bash
git clone https://github.com/rabeyaasif-aiml/GlamBase.git
cd GlamBase
```

### 2. Set up the database

```bash
mysql -u root -p < database/schema.sql
```

### 3. Set up the backend

```bash
cd backend
python -m venv venv
venv\Scripts\activate        # Windows
pip install -r requirements.txt
```

Create a `.env` file in the `backend` folder:

```env
DB_HOST=localhost
DB_USER=your_mysql_username
DB_PASSWORD=your_mysql_password
DB_NAME=glambase
```

Run the server:

```bash
python app.py
```

### 4. Set up the frontend

```bash
cd frontend
npm install
npm start
```

The app will be running at `http://localhost:3000`.

## 📁 Project Structure

```
GlamBase/
├── backend/
│   ├── app.py
│   ├── requirements.txt
│   └── .env            # not committed
├── frontend/
│   ├── src/
│   ├── public/
│   └── package.json
├── database/
│   └── schema.sql
├── .gitignore
└── README.md
```

## 🔮 Future Improvements

- User authentication and roles
- Payment integration
- Product search and filters
- Deployment (frontend + backend + hosted database)

## 👩🏻‍💻 Author

**Rabeya Asif**
Software Engineering student at IOBM

- GitHub: [@rabeyaasif-aiml](https://github.com/rabeyaasif-aiml)
- LinkedIn: [rabeya-asif-ml](https://linkedin.com/in/rabeya-asif-ml)

---

⭐ If you found this project interesting, feel free to star the repo!
