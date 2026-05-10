# 💊 Pharmacy Management System (ADBMS)📌 

## Project Overview
This is a professional-grade Windows Forms application developed for the 6th-semester Advanced Database Management Systems (ADBMS) project. The system is designed to automate pharmacy operations, including inventory tracking, supplier management, and automated sales billing with integrated discount logic.

## 📂 Repository Structure
The project is organized into a modular architecture to ensure scalability and ease of maintenance:
### /Database: 
Contains the master SQL script (script (3).sql) including schema definitions, data seeding, and stored procedures.

## /Forms: 
Contains the UI Triad files (.cs, .Designer.cs, .resx) for all 7 application screens, along with Program.cs and DBConnection.cs.  

## harmacyManagementSystem.csproj: 
The project configuration file that manages dependencies and build settings.  

## 🛠️ Tech StackFramework: 
.NET 10.0 Windows Forms.  Database: Microsoft SQL Server.
## Language: 
C# (C-Sharp).Libraries: Microsoft.Data.SqlClient (v7.0.1).  

## 🧠 Core Features & LogicDynamic Inventory Tracking: 
Uses SQL CASE statements to categorize stock as 'Available', 'Low Stock', or 'Expired' in real-time.Automated Discount 
## Engine: 
Implements a multi-tier discount system (5%, 10%, and 15%) handled directly within the database logic.

## Relational Integrity: 
Utilizes Foreign Keys, Unique constraints, and CHECK constraints to ensure pharmaceutical data accuracy.

## Secure Authentication: 
Role-based access (Admin/Staff) verified through hashed database queries.  

## 🚀 Setup InstructionsClone the Repo: 
Download the project files to your local machine.
## Initialize Database: 
Run the script in the /Database folder in your SQL Server instance.

## Update Connection String: 
Modify the DBConnection.cs file to match your local SQL Server instance name.  Run Application: Open the .csproj file in Visual Studio and press Start.  

## 📜 License
This project is licensed under the MIT License-free for educational and modification purposes.
