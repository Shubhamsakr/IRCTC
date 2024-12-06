# IRCTC
This is a backend API for a railway management system like IRCTC. It allows users to check train availability, book seats, and view bookings while supporting role-based access for admins.

Features
User Registration & Login (with JWT authentication)
Admin Functions:
Add new trains
User Functions:
Check seat availability
Book seats
View booking details
Handles race conditions for simultaneous bookings.
Tech Stack
Framework: Flask
Database: PostgreSQL
ORM: SQLAlchemy
Authentication: JWT
Setup Instructions
Prerequisites
Python 3.9+
PostgreSQL installed and running
Steps
Clone the repository:

bash
Copy code
git clone <repo_url>
cd <repo_directory>
Install dependencies:

bash
Copy code
pip install -r requirements.txt
Configure .env file with the following:

php
Copy code
DATABASE_URI=postgresql://<username>:<password>@localhost/<database_name>
JWT_SECRET_KEY=<your_jwt_secret_key>
ADMIN_API_KEY=<your_admin_api_key>
Set up the database:

bash
Copy code
flask db upgrade
Run the server:

bash
Copy code
python app.py
API Endpoints
Authentication
Register: POST /register
Login: POST /login
Admin (Protected by API Key)
Add Train: POST /trains
User
Check Availability: GET /availability
Book Seat: POST /book (JWT required)
View Booking: GET /booking/<booking_id> (JWT required)
Testing
Use tools like Postman or cURL to test API endpoints.
Automated tests can be run using pytest.
License
This project is for evaluation purposes only.
