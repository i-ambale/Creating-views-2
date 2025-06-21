#📘 README: Creating Views – Exercise 2 with Northwind.db
## 🧠 Project Title
Mastering SQL Views with Northwind: Exercise 2 on Creating, Using, and Updating Views

## 📝 Description
This project deepens your understanding of **SQL views** using the popular `Northwind.db` sample database. You will learn how to create, query, and update views as part of real-world data modeling and reporting tasks in a relational database environment.

| ⚠️ This project is designed to run **locally** using SQLite and cannot be executed on Google Colab without adaptations.

## 🎯 Learning Objectives
By the end of this exercise, you will be able to:

- ✅ Create **views** that encapsulate complex queries

- ✅ Query views as if they were tables

- ✅ **Update** views by dropping and recreating them

- ✅ Understand the role of views in **database design and abstraction**

## 📦 Requirements
### 💻 Tools
- SQLite3 or DB Browser for SQLite

- Jupyter Notebook or any SQL-enabled IDE (e.g., VS Code)

### 📁 Dataset
- Northwind.db  
  Download the SQLite sample database from:
 [ https://github.com/jpwhite3/northwind-SQLite](https://docs.yugabyte.com/preview/sample-data/northwind/)

## 🧱 Project Structure
```
.
├── views_exercise_2.ipynb       # Main notebook for creating views
├── README.md                    # Project guide and instructions
├── Northwind.db                 # SQLite sample database (must be downloaded separately)
└── sql/                         # Optional SQL scripts for reference
```

## 🔧 How to Use
1. Download `Northwind.db` and place it in the same folder as the notebook or script.

2. Open the `views_exercise_2.ipynb` notebook in your preferred SQL environment.

3. Follow along with the exercises:

    - Create a view
    
    - Query the view
    
    - Drop and recreate the view with enhancements
  
## 🧪 Sample Exercises
✅ **1. Create a View of High-Value Customers**
```
CREATE VIEW HighValueCustomers AS
SELECT 
    c.CompanyName,
    c.ContactName,
    SUM(o.Freight) AS TotalFreight
FROM Customers c
JOIN Orders o ON c.CustomerID = o.CustomerID
GROUP BY c.CustomerID
HAVING TotalFreight > 100;
```
✅ **2. Query the View**
```
SELECT * FROM HighValueCustomers;
```
🧹 **3. Drop and Recreate the View (If Needed)**
```
DROP VIEW IF EXISTS HighValueCustomers;
```

## 📚 Why Use Views?
- Simplifies **repetitive queries**

- Helps enforce **data security** by restricting access to specific columns

- Promotes clean, **maintainable SQL design**

- Abstracts away complexity from business analysts or end users

## 📧 Contact
**Author**: Ibrahim Ambale
📍 Nairobi, Kenya
🔗 LinkedIn: [Ibrahim Ambale](https://linkedin.com/in/ibrahim-ambale/)
