# MyLibrary
# MyLibrary Desktop Application
## Overview

**MyLibrary** is a Windows desktop application developed in C# using WinForms. It manages a small library's book inventory and member borrowing records. This project demonstrates event-driven programming, UI design, and database integration using ADO.NET with SQL Server LocalDB.
## Features

- **User Authentication**
  - Login form with username and password validation against the database.
- **Books Management**
  - View, add, edit, and delete books.
  - Fields include BookID, Title, Author, Year, and AvailableCopies.
  - Input validation ensures data integrity.
- **Borrowers Management**
  - View, add, edit, and delete borrowers.
  - Fields include BorrowerID, Name, Email, Phone.
- **Issue and Return Books**
  - Issue books to borrowers, updating available copies and tracking issue/return dates.
  - Return books and update records accordingly.
---
## Technologies Used

- **Language & Framework:** C# (.NET Framework), Windows Forms (WinForms)
- **Database:** SQL Server LocalDB
- **Data Access:** ADO.NET with parameterized SQL queries
- **Development Environment:** Visual Studio 2022 or later

---

## Setup and Installation

### Prerequisites

- Windows OS
- Visual Studio 2022 or later with .NET Desktop Development workload
- SQL Server LocalDB (standalone)
