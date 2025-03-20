
# Database Schema for E-Commerce Sales



## Table Creation Scripts (DDL)

### 1. Customers Table
- This table stores customer information.

```sql
CREATE TABLE Customers (
    CustomerID INT IDENTITY(1,1) PRIMARY KEY,
    CustomerName VARCHAR(100),
    Email VARCHAR(100),
    Phone VARCHAR(20),
    City VARCHAR(50),
    Country VARCHAR(50)
);

- CustomerID: Unique identifier for each customer (Primary Key).
- CustomerName: Full name of the customer.
- Email: Customer’s email address.
- Phone: Contact number of the customer.
- City: City of residence.
- Country: Country of residence

```
### 2. Products Table

```sql
CREATE TABLE Products (
    ProductID INT IDENTITY(1,1) PRIMARY KEY,
    ProductName VARCHAR(100),
    Category VARCHAR(50),
    Price DECIMAL(10,2),
    StockQuantity INT
);

- ProductID: Unique identifier for each product (Primary Key).
- ProductName: Name of the product.
- Category: Category to which the product belongs.
- Price: Price of the product (up to 10 digits with 2 decimal places).
- StockQuantity: Number of items available in stock.

```
### 3. Sales Table

```sql

CREATE TABLE Sales (
    SaleID INT IDENTITY(1,1) PRIMARY KEY,
    CustomerID INT,
    ProductID INT,
    SaleDate DATE,
    Quantity INT,
    TotalAmount DECIMAL(10,2),
    FOREIGN KEY (CustomerID) REFERENCES Customers(CustomerID),
    FOREIGN KEY (ProductID) REFERENCES Products(ProductID)
);


- SaleID: Unique identifier for each sale (Primary Key).
- CustomerID: References the Customers table (Foreign Key).
- ProductID: References the Products table (Foreign Key).
- SaleDate: Date when the sale was made.
- Quantity: Number of units sold.
- TotalAmount: Total price of the sale.
