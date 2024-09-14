# CRUDFUSION

**CRUDFUSION** is a project that demonstrates basic CRUD (Create, Read, Update, Delete) operations on a SQL database. It uses an Apache server to host the application, with SQL as the database backend, and Python as the primary programming language for connectivity and handling requests.

## Features
- Create new records in the database
- Retrieve and display records from the database
- Update existing records
- Delete records from the database

## Technologies Used
- **Apache Server**: Web server used to host the application.
- **SQL**: For database management and operations.
- **Python**: Handles CRUD operations and connects to the SQL database.

## Installation

### Prerequisites
1. **Apache Server** installed and running on your machine.
2. **Python** installed (version 3.x recommended).
3. **Python SQL connector** package installed (e.g., `mysql-connector-python` for MySQL).

### Steps to Install
1. Clone the repository:
    ```bash
    git clone https://github.com/SakshamAggarwal101002/CRUDFUSION.git
    cd CRUDFUSION
    ```

2. Install required Python packages:
    ```bash
    pip install mysql-connector-python
    ```

3. Set up your SQL database:
    ```sql
    CREATE DATABASE crudfusion_db;
    USE crudfusion_db;

    CREATE TABLE users (
        id INT AUTO_INCREMENT PRIMARY KEY,
        name VARCHAR(255) NOT NULL,
        email VARCHAR(255) NOT NULL UNIQUE
    );
    ```

4. Configure the connection settings in the Python script. Modify the following section in `crudfusion.py`:
    ```python
    db_config = {
        'user': 'your-username',
        'password': 'your-password',
        'host': 'localhost',
        'database': 'crudfusion_db'
    }
    ```

5. Run the Python application:
    ```bash
    python crudfusion.py
    ```

6. Ensure Apache is running:
    ```bash
    sudo service apache2 start
    ```

7. Access the application from your browser:
    ```
    http://localhost/CRUDFUSION
    ```

## CRUD Operations Overview

### 1. **Create**
   - Adds new entries to the database.
   - Example SQL query:
     ```sql
     INSERT INTO users (name, email) VALUES ('John Doe', 'john@example.com');
     ```

### 2. **Read**
   - Fetches data from the database.
   - Example SQL query:
     ```sql
     SELECT * FROM users;
     ```

### 3. **Update**
   - Modifies existing records in the database.
   - Example SQL query:
     ```sql
     UPDATE users SET name = 'Jane Doe' WHERE id = 1;
     ```

### 4. **Delete**
   - Deletes records from the database.
   - Example SQL query:
     ```sql
     DELETE FROM users WHERE id = 1;
     ```

## Directory Structure

