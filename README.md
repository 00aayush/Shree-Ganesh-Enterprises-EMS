# Shree-Ganesh-Enterprises-EMS
Employee Management System (EMS)
This document outlines the plan to build the Employee Management System (EMS) web application using HTML, CSS, JavaScript, and MySQL.

Goal Description
Create a web-based Employee Management System (EMS) that supports two user roles: Admin and Employee. The frontend will be built using modern web design principles (vibrant colors, glassmorphism, smooth animations) and Vanilla technologies (HTML, CSS, JS).

To support the requested MySQL database, we will introduce a lightweight Node.js (Express) backend. This server will act as an API bridge between your frontend and the MySQL database, as frontend JavaScript cannot securely or directly connect to MySQL.

User Review Required
IMPORTANT

Since this is a completely new project and you don't have an active workspace, I will create this project in a new directory at C:\Users\paraj\.gemini\antigravity\scratch\ems-app. You can later set this as your active workspace.

CAUTION

Architectural Change: Browsers cannot connect directly to MySQL databases. Therefore, I will create a simple Node.js backend server to handle the database queries. You will need to have Node.js and MySQL installed and running on your Windows machine. I will set up the database connection using the provided credentials (root/root).

Open Questions
IMPORTANT

Authentication: Should we build a simple login screen where you type an ID to log in, or just a simple toggle button for testing purposes to switch between Admin and Employee views?
Design Theme: Do you prefer a sleek Dark Mode or a clean Light Mode for the premium aesthetic?
Database Setup: I will provide a SQL script to create the database and tables. Do you want me to run it automatically, or will you set up the MySQL database manually?
Proposed Changes
We will create the following file structure for the application:

Backend Files
[NEW] server/package.json & server/server.js
A lightweight Node.js Express server to expose REST APIs for the frontend.

[NEW] server/db.js
Handles the MySQL connection using the mysql2 package with credentials root / root.

[NEW] database.sql
A SQL script to initialize the tables (employees, attendance, tasks).

Frontend Files (in public/ directory)
[NEW] public/index.html
The main HTML structure containing the login view and the dashboard views for both Admin and Employee.

[NEW] public/styles.css
The stylesheet containing premium, modern UI designs.

[NEW] public/js/app.js
The core JavaScript file that handles API calls to the Node.js backend and UI state changes.

[NEW] public/js/admin.js
Contains logic for the Admin dashboard interacting with the API (add employee, assign work, manage attendance).

[NEW] public/js/employee.js
Contains logic for the Employee dashboard interacting with the API (mark attendance, view work).

Verification Plan
Automated Tests
N/A for this phase.
Manual Verification
I will set up the Node.js server and connect it to your local MySQL.
We will start the server and open the application in the browser.
We will manually test the complete flow and verify data is correctly saved to and retrieved from MySQL.
