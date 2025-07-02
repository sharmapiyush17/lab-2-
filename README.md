Record Store Inventory - JavaFX & MySQL
Developer: Piyush Piyush
Student ID: 22050267
Date: 2025-06-05
Some help is taken from Gemini

This is a JavaFX application connected to a MySQL database, allowing users to manage a record store's inventory (CRUD operations on music records).

📌 Features
Display all records in a table (ID, Title, Format, Price)

Insert new records

Update existing records

Delete selected records

View full database contents

JavaFX GUI for desktop interaction

MySQL database backend (with JDBC)

🧩 Technologies Used


JavaFX

MySQL

JDBC



Setup Instructions
Step 1: MySQL Database Setup
Create a database called recordstore:

sql
Copy
Edit
CREATE DATABASE recordstore;
USE recordstore;

CREATE TABLE Records (
    record_id INT AUTO_INCREMENT PRIMARY KEY,
    title VARCHAR(100),
    format VARCHAR(50),
    purchase_price DOUBLE
);
(Optional) Add sample data:

sql
Copy
Edit
INSERT INTO Records (title, format, purchase_price)
VALUES 
('Dark Side of the Moon', 'LP', 5.00),
('Abbey Road', 'CD', 6.50);
✅ Step 2: Java Project Setup
Open your project in IntelliJ, Eclipse, or NetBeans.

Add MySQL Connector/J to your project:

Download Connector

Add the .jar file to your build path.

✅ Step 3: Edit Database Credentials (in connectToDatabase())
java
Copy
Edit
conn = DriverManager.getConnection(
    "jdbc:mysql://localhost:3306/recordstore",
    "root",
    "1234"
);
Replace "root" and "1234" with your actual MySQL username and password.

✅ Step 4: Run the Application
Run RecordStoreApp.java

GUI opens showing the inventory table

Add, update, delete records and view them live

📷 Screenshots to Include in Submission
GUI layout with:

TableView

Insert/Update/Delete/View buttons

Footer with Name, ID, Date

JDBC connection code

Inserting a record and it appears in table

Updating a record and showing new data

Deleting a record and it disappears

View Data populates the table.
