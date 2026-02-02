Zoo Admin Pro: Hybrid Management System
A comprehensive, dual-platform management system designed for modern zoos, this project features a Web Interface (JSP) for mobile accessibility and a Desktop Dashboard (Python) for advanced data analytics and reporting.

Overview
This project bridges the gap between field work and administrative analysis. Both applications connect to a centralized MySQL database, ensuring real-time data synchronization.

Web Module (JSP): Designed for mobile inventory management and daily logging.

Desktop Module (Python): Designed for administrators to visualize health trends and generate PDF medical reports.

Important: Configuration
To ensure the application connects to your local database, you must update the credentials in both modules:

1. In Python (ZooDashboard.py):
Find the get_db_connection method and replace the placeholders with your MySQL data:

Python
host="localhost",
user="YOUR_USERNAME",  # e.g., "root"
password="YOUR_PASSWORD", 
database="gradina_zoologica"
2. In JSP (JavaBean/Connection class):
Update the connection string in your Java source file:

Java
String url = "jdbc:mysql://localhost:3306/gradina_zoologica";
String user = "YOUR_USERNAME";
String password = "YOUR_PASSWORD";
🛠️ Technology Stack
Database: MySQL (Relational storage).

Web: Java Server Pages (JSP), Apache Tomcat, JDBC.

Desktop: Python 3.x, CustomTkinter (UI), Matplotlib (Charts), FPDF (PDF Generation).

Key Features
Centralized Inventory: Real-time sync between Web and Desktop.

Medical Alerts: Automatic detection of animals needing check-ups.

Analytics: Visual distribution of species and weight history.

Security: Implements Parameterized Queries to prevent SQL Injection.

Installation
Database: Import the provided .sql files into your MySQL server.

Web App: Deploy the JSP folder to the Tomcat webapps directory.

Desktop App: * Install requirements: pip install customtkinter mysql-connector-python matplotlib fpdf pillow

Run: python ZooDashboard.py

License
This project is open source.

Author
Andreea Zbranca
