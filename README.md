# Criminal Record Management System

This is a **Criminal Record Management System** built using Python with a Tkinter GUI and MySQL for database management. The system supports multiple user roles (Police and Victim) and provides various functionalities such as managing cases, handling complaints, visualizing data, and maintaining an audit trail for case updates.


## Features

### 1. **User Authentication**
- Role-based access control (Police and Victim).
- Login system with username and password validation.

### 2. **Police Dashboard**
- Manage cases: Add, update, and view case statuses.
- Handle complaints: Add new complaints, view complaints, and update their status.
- Visualize case statuses using bar graphs.
- View related cases and complaints (unresolved ones).

### 3. **Victim Dashboard**
- Victims can view their own cases and complaints.

### 4. **Database Operations**
- Nested joins and aggregation queries for related cases and complaints.
- Audit trail using MySQL triggers for case status changes.
- Stored procedure to add complaints.

---

## Installation

### Prerequisites
1. **Python 3.x**
2. **MySQL Server**
3. Required Python modules:
   - `tkinter`
   - `mysql-connector-python`
   - `matplotlib`

### Steps
1. Clone the repository:
   git clone <repository_url>
   cd criminal_record_management_system
2. Install the required Python packages:
   pip install mysql-connector-python matplotlib
3. Configure the database:
   Create a MySQL database named criminal_record_db.
   Update the database credentials in the db_config dictionary in the code:
   db_config = {
    'host': 'localhost',
    'user': 'your_mysql_username',
    'password': 'your_mysql_password',
    'database': 'criminal_record_db'
  }
  Import the database schema (e.g., schema.sql) to create the necessary tables:
  mysql -u root -p criminal_record_db < schema.sql
5. Run the application:
  python <main_script_name>.py

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
  git checkout -b feature_name
3. Commit your changes:
  git commit -m "Add your message here"
4. Push to the branch:
  git push origin feature_name
5. Create a pull request.

## Future Enhancements
Add encryption for sensitive data.
Implement REST APIs for external integrations.
Improve UI/UX for better usability.
Can be extended to include detailed tables for victims and accused.


Make sure to replace placeholders like <repository_url>, schema.sql, <main_script_name>.py, and your contact details with actual values.

