# 🔐 Criminal Record Management System

A **Criminal Record Management System** built using **Python (Tkinter)** for the GUI and **MySQL** for database management. It supports **role-based access control** (Police and Victim) and offers functionalities like case management, complaint handling, data visualization, and audit trails through triggers.

---

## 🚀 Features

### 👥 User Authentication
- Secure login system with username and password validation
- Role-based access: Police and Victim

### 👮 Police Dashboard
- Add, update, and view case statuses
- File and manage complaints
- View unresolved cases and complaints
- Visualize data with bar graphs (using `matplotlib`)

### 🙋 Victim Dashboard
- View personal case and complaint records

### 🧩 Database Operations
- Nested joins and aggregation queries for linked cases and complaints
- MySQL trigger-based **audit trail** for tracking case status updates
- Stored procedures for efficient complaint insertion

---

## 🛠️ Installation

### Prerequisites
- **Python 3.x**
- **MySQL Server**
- Python packages:
  - `tkinter`
  - `mysql-connector-python`
  - `matplotlib`

### Setup Steps

1. **Clone the Repository**
   ```bash
   git clone https://github.com/HannahAlex004/Criminal-Record-Information-System.git
   cd criminal_record_management_system
   ```
2. Install the required Python packages:
   ```bash
   pip install mysql-connector-python matplotlib
   ```
4. Configure the database:
   Create a MySQL database named criminal_record_db.
   Update the database credentials in the db_config dictionary in the code:
   ```bash
   db_config = {
    'host': 'localhost',
    'user': 'your_mysql_username',
    'password': 'your_mysql_password',
    'database': 'criminal_record_db'
  }
  ```
  Import the database schema (e.g., schema.sql) to create the necessary tables:
```bash
  mysql -u root -p criminal_record_db < schema.sql
````
6. Run the application:
   ```bash
  python codes.py
```
## Database Design
### Tables
Users: Stores user information and roles.
Cases: Contains case details such as type, description, and status.
Complaints: Links complaints to cases and tracks their resolution.
CaseHistory: Records the audit trail of case status updates.
### Code Structure
HomePage: The landing page of the application.
LoginWindow: Handles user authentication.
PoliceDashboard: Main interface for police officers.
VictimDashboard: Interface for victims to view their cases and complaints.
ComplaintManagement: Module for handling complaints.
Trigger: A MySQL trigger for tracking changes in case statuses.
Stored Procedure: Adds new complaints efficiently.
### Graph Visualization
The app uses matplotlib to generate:
Bar charts of case statuses for better visualization of data.

## How to Contribute
1. Fork the repository.
2. Create a new branch for your feature/bug fix:
```bash
  git checkout -b feature_name
```
3. Commit your changes:
   ```bash
  git commit -m "Add your message here"
  ```
5. Push to the branch:
```bash
  git push origin feature_name
```
6. Create a pull request.

## Future Enhancements
Add encryption for sensitive data.
Implement REST APIs for external integrations.
Improve UI/UX for better usability.
Can be extended to include detailed tables for victims and accused.


