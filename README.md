# Centralized Doctor-Patient Appointment Portal

## Project Overview
This is a web-based portal for centralized doctor-patient appointment scheduling. The application allows patients to book appointments with doctors, and doctors to manage their bookings. It features user authentication, appointment management, and a simple search for doctors by name.

## Features
- User authentication (Doctor/Patient)
- Book, edit, and delete appointments
- Doctor and patient management
- Search for doctors by name
- Responsive UI using Bootstrap

## Tech Stack
- **Backend:** Python (Flask)
- **Frontend:** HTML, CSS, Bootstrap
- **Database:** MySQL

## Dependencies
Install the following Python packages:
- Flask
- Flask-Login
- Flask-SQLAlchemy
- mysqlclient

You can install them using pip:
```bash
pip install Flask Flask-Login Flask-SQLAlchemy mysqlclient
```
If you are on Windows and face issues with `mysqlclient`, you can use `PyMySQL`:
```bash
pip install Flask Flask-Login Flask-SQLAlchemy PyMySQL
```

## Database Setup
1. Make sure you have MySQL installed and running.
2. Create a database named `cdpap` (or as configured in `main.py`).
3. Import the provided `cdpap.sql` file to set up the tables and sample data:
   ```bash
   mysql -u root -p cdpasp < cdpap.sql
   ```

## How to Run
1. Ensure all dependencies are installed and the database is set up.
2. Update the MySQL connection string in `main.py` if your credentials differ:
   ```python
   app.config['SQLALCHEMY_DATABASE_URI'] = 'mysql://root:@localhost/cdpap'
   ```
3. Start the Flask application:
   ```bash
   python main.py
   ```