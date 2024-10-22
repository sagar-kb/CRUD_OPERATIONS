# Java JDBC CRUD Operations

This project demonstrates how to perform basic CRUD (Create, Retrieve, Update, Delete) operations on a MySQL database using Java JDBC. The project contains separate Java files for each operation: inserting new records, retrieving all records, updating existing records, and deleting records from the database.

## Features

- **Create**: Insert new records into the database using `PreparedStatement`.
- **Retrieve**: Fetch and display all records from the database.
- **Update**: Modify existing records by updating specific fields.
- **Delete**: Remove records from the database based on user input.

## Project Structure

1. **create.java**: 
   - Establishes a connection to the MySQL database.
   - Executes a `SELECT` query to retrieve all records from the `stu` table.

2. **delete.java**:
   - Prompts the user to enter a student ID.
   - Deletes the record corresponding to the provided ID from the `stu` table.

3. **insert.java**:
   - Takes user input for student ID, name, and marks for three subjects.
   - Inserts the provided data as a new record into the `stu` table.

4. **retrive.java**:
   - Fetches and displays all records from the `stu` table, showing student ID, name, and marks for three subjects.

5. **update.java**:
   - Prompts the user for a student ID and new marks for three subjects.
   - Updates the corresponding record in the `stu` table with the provided marks.

## Database Setup

Before running the project, make sure you have set up the MySQL database and table:

1. Create a MySQL database named `jdbc`:
    ```sql
    CREATE DATABASE jdbc;
    ```

2. Use the `jdbc` database:
    ```sql
    USE jdbc;
    ```

3. Create the `stu` table:
    ```sql
    CREATE TABLE stu (
        id INT PRIMARY KEY,
        name VARCHAR(50),
        marks1 INT,
        marks2 INT,
        marks3 INT
    );
    ```

## How to Run

1. Clone the repository or download the project files.
2. Make sure you have the MySQL JDBC driver in your classpath.
3. Update the connection details in each Java file as needed (`jdbc:mysql://localhost:3306/jdbc`, username: `root`, password: `root`).
4. Compile and run the desired Java file from your terminal or IDE:
