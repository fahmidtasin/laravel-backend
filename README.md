## Laravel Backend - Users API (CRUD)

This is a Laravel backend project providing a RESTful API for managing users.
It is designed to work with a React frontend (or any frontend) for full-stack CRUD operations using MySQL as the database.

---

## Features

- Laravel 10+ backend

- RESTful API endpoints for Users

- CRUD operations: Create, Read, Update, Delete

- MySQL database support

- Ready for integration with React or any frontend

- CORS configured for frontend access

## API Endpoints
```bash
| Method | Endpoint          | Description             |
| ------ | ----------------- | ----------------------- |
| GET    | `/api/users`      | Get all users           |
| GET    | `/api/users/{id}` | Get a single user       |
| POST   | `/api/users`      | Create a new user       |
| PUT    | `/api/users/{id}` | Update an existing user |
| DELETE | `/api/users/{id}` | Delete a user           |
```
---

## Installation

Clone the repository:
```bash
git clone https://github.com/fahmidtasin/laravel-backend.git
```

## Project Run
1. Go into the project folder:
```bash
cd laravel-backend
```

2. Install dependencies:
```bash
composer install
```

3. Create .env file and configure database:
```bash
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=react_crud
DB_USERNAME=root
DB_PASSWORD=
```

4. Run migrations:
```bash
php artisan migrate
```

5. Start the development server:
```bash
php artisan serve
```

Server will run at: http://localhost:8000

---

## CORS Setup

CORS is already configured to allow access from frontend (React):

// config/cors.php
```bash
'paths' => ['api/*'],
'allowed_methods' => ['*'],
'allowed_origins' => ['http://localhost:5173'],
'allowed_headers' => ['*'],
```
---
## Usage

Use Axios or Fetch from your frontend to call the API endpoints.

Example with Axios:
```bash
import axios from 'axios';

const users = await axios.get('http://localhost:8000/api/users');
```
---
## Project Structure
```bash
laravel-backend/
│
├─ app/
│  ├─ Http/
│  │  └─ Controllers/UserController.php
│  └─ Models/User.php
│
├─ database/
│  └─ migrations/
├─ routes/
│  └─ api.php
├─ .env
├─ composer.json
└─ artisan
```
## Notes

Make sure MySQL is running (XAMPP or other).

Make sure frontend runs on http://localhost:5173
 (for CORS).