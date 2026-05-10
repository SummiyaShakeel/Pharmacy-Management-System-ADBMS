# 🖥️ Application UI & Logic (Forms)
This folder contains the User Interface (UI) and Frontend Logic for the Pharmacy Management System. The application is built using C# Windows Forms on the .NET 10.0 framework.  
## 📂 Folder Structure
Each screen in this folder consists of three core files:
#### .cs: The backend logic (event handlers, SQL connections, and validation).
#### .Designer.cs: Automatically generated code that defines the UI layout and controls.  
#### .resx: XML-based resource files that store UI metadata.  
## 📋 Screen Overview1. 
### 1.User Authentication (login.cs)
Purpose: Secure gateway for Admin and Staff access.
Logic: Uses a SELECT COUNT(*) query to verify credentials against the Users table.  Feature: Implements UseSystemPasswordChar for secure password entry. 
### 2. Main Dashboard (screen2.cs)
Purpose: The central navigation hub of the application.  
Logic: Handles form switching logic, allowing users to jump between different management modules while hiding the dashboard to keep the workspace clean.  
### 3. Medicine Management (Screen3.cs)
Purpose: Core inventory CRUD operations (Add, Update, Delete, View).  
Logic: Includes robust data validation to ensure prices are decimal and quantities are integers before database submission.  
### 4. Supplier Management (Screen4.cs)
Purpose: Manages pharmaceutical distributor contact details.  
Logic: Linked directly to the Suppliers table, allowing for real-time updates of vendor information.  
#### 5. Sales & Billing (Screen5.cs)
Purpose: Handles customer transactions and invoice generation.  
Logic: Features a dynamic grandTotal calculator that updates as items are added to the bill. It includes a Batch No field to ensure correct stock tracking.  
### 6. Inventory Tracking (Screen6.cs)
Purpose: Advanced monitoring of stock health.  
Logic: Uses a SQL CASE statement to dynamically categorize items as 'Expired', 'Low Stock', or 'Available' based on GETDATE() and quantity thresholds.  
### 7. Reports Management (Screen7.cs)
Purpose: Generates business insights (Sales, Stock, and Expiry reports).  
Logic: Implements a selection-based report generator that confirms successful data processing via user alerts.  
## 🛠️ Global Logic ModulesDBConnection.cs: 
A centralized class providing the SqlConnection string. It uses Integrated Security for local development.  
### Program.cs: 
The entry point of the application, configured to launch the login form first.  
