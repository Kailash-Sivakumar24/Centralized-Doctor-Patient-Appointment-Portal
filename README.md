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

### Local Development
1. **Install XAMPP**: Download and install XAMPP from [https://www.apachefriends.org/](https://www.apachefriends.org/)
2. **Start XAMPP Services**:
   - Open XAMPP Control Panel
   - Start Apache and MySQL services
   - Ensure both services show green status
3. **Access phpMyAdmin**:
   - Open your web browser
   - Go to `http://localhost/phpmyadmin`
4. **Create Database**:
   - Click on "New" in the left sidebar
   - Enter database name: `cdpap`
   - Click "Create"
5. **Import SQL File**:
   - Select the newly created `cdpap` database from the left sidebar
   - Click on the "Import" tab at the top
   - Click "Choose File" and select the `cdpap.sql` file from your project directory
   - Click "Go" at the bottom to import the database structure and sample data
6. **Verify Import**: You should see the tables created successfully in the database

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
