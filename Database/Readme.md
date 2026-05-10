# 🗄️ Database Documentation
This folder contains the complete SQL schema and initialization scripts for the Pharmacy Management System.

## 📄 Files
script (3).sql: The master script containing all Table definitions, Constraints, Stored Procedures, and the Billing Logic.

## 🛠️ Setup Instructions
Open SSMS: Open Microsoft SQL Server Management Studio.

### Create Directory: 
Ensure the path D:\PharmacyDB\ exists on your machine, as the script is configured to save the .mdf and .ldf files there.

### Execute Script: 
Open script (3).sql and run it to create the PharmacyDB database.


### Connection String: 
Ensure your DBConnection.cs in the C# project matches your local server instance (e.g., .\SQLEXPRESS).  

## 📐 Schema Design
The database is designed with a focus on Data Integrity and Automation:

### Tables: 
Includes Users for authentication, Medicines for inventory, and Suppliers for vendor tracking.

### Relationships: 
Implements Primary Keys and Unique constraints on Usernames and Emails to prevent duplicate data.

### Constraints: 
Medicines are protected by logic that prevents negative pricing or stock quantities.

## 🧠 Advanced Logic
This project goes beyond basic storage by implementing backend business logic:

### Automated Discount Engine: 
A built-in script calculates total bills and applies tiered discounts:

5% Discount for bills between 5,000 and 10,000.

10% Discount for bills between 10,000 and 15,000.

15% Discount for bills exceeding 15,000.


Dynamic Status Handling: The inventory system uses SQL CASE logic to flag low stock and expired items in real-time.
