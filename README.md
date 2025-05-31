Etsubdink Mekete 1501178
##MyLibrary Desktop Application
This repository contains the source code for "MyLibrary," a Windows desktop application developed in C# using WinForms. It is designed to manage a small library's book inventory and member borrowing records, demonstrating event-driven programming, UI design, and database connectivity with SQL Server LocalDB.

##Features
"MyLibrary" provides the following core functionalities:

Login System: Secure authentication against a Users table.

##Books Management:

Display a list of all books with details (ID, Title, Author, Year, Available Copies).

Add new book records.

Edit existing book details.

Delete book records.

Input validation for all fields.

##Borrowers Management:

Display a list of all registered borrowers (ID, Name, Email, Phone).

Add new borrower records.

Edit existing borrower details.

Delete borrower records.

Input validation for all fields.
###Technical Stack
Language: C#

Framework: .NET Framework (WinForms)

Database: SQL Server LocalDB

Data Access: ADO.NET with parameterized queries

UI Design: Windows Forms (WinForms)

##Database Setup
The application uses a SQL Server LocalDB instance.

##Database Server
The default database server name used in this project is:(LocalDB)\MSSQLLocalDB
#Database Schema
You will find a .sql file (LibraryMnagementSystem.sql) in the root of this repository. This script will create the necessary database and tables.

Steps to create the database:

Open SQL Server Management Studio (SSMS) or Visual Studio's SQL Server Object Explorer.

Connect to the (LocalDB)\MSSQLLocalDB server.

Open the LibraryMnagementSystem.sql file.

Execute the script to create the LibraryMnagementSystem database and its tables.

The database will contain the following tables:

Users: Stores user credentials for login.

UserID (INT, PK)

Username (NVARCHAR(50))

Password (NVARCHAR(255)) 

Books: Stores details of all books in the library.

BookID (INT, PK)

Title (NVARCHAR(255))

Author (NVARCHAR(255))

PublicationYear (INT)

AvailableCopies (INT)

TotalCopies (INT)

Borrowers: Stores information about library members.

BorrowerID (INT, PK)

Name (NVARCHAR(255))

Email (NVARCHAR(255))

Phone (NVARCHAR(20))

IssuedBooks: Records all book borrowing transactions.

IssueID (INT, PK)

BookID (INT, FK to Books)

BorrowerID (INT, FK to Borrowers)

IssueDate (DATE)

DueDate (DATE)

ReturnDate (DATE, NULLABLE) 

##Default Login Credentials
After running the database script, the Users table will be seeded with default credentials for testing:

Username: abebe

Password: admin123

Installation and Running
Prerequisites
Visual Studio: 2019 or later (with .NET desktop development workload installed).

.NET Framework: Ensure the correct .NET Framework version (e.g., 4.7.2 or 4.8) is installed, as specified in the project file.

SQL Server LocalDB:

##Steps to Run
Clone the Repository:

git clone https://github.com/m-12-e/MyLibrary.git
cd MyLibrary

Create Database: Follow the Database Setup instructions to create the LibraryMnagementSystem database and tables using the provided .sql script.

Open in Visual Studio:

Open the Library.sln solution file in Visual Studio.

Configure Connection String:

Locate the App.config file in the main project.

Build the Solution:

In Visual Studio, go to Build > Build Solution (or press Ctrl+Shift+B). This will compile the project and resolve any dependencies.

Run the Application:

Go to Debug > Start Debugging (or press F5).

The Login Form will appear.

Usage Guide
Login:

Enter the default credentials (abebe/admin123) to access the main application.

An error message will be displayed for invalid credentials.

Main form:

The main window features a tabbed interface (or menu) for "Books Management" and "Borrowers Management".

Books Management:

The DataGridView displays all books.

Add Book: Click "Add Book" to open a form. Fill in details and save. Input validation will prevent empty fields or invalid data.

Edit Book: Select a row in the DataGridView and click "Edit Book". The form will pre-populate with the selected book's details for modification.

Delete Book: Select a row and click "Delete Book". A confirmation prompt will appear before deletion.

Borrowers Management:

Similar to Books Management, you can Add, Edit, and Delete borrower records.


