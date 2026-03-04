# Food Ordering System

## Monorepo Structure

This repository is organized as a monorepo containing both the Laravel backend and the React frontend. The structure is as follows:

```
food-ordering-system/
├── backend/        # Laravel application
│   ├── app/
│   ├── bootstrap/
│   ├── config/
│   ├── database/
│   ├── public/
│   ├── resources/
│   ├── routes/
│   ├── storage/
│   └── tests/
├── frontend/       # React application
│   ├── public/
│   ├── src/
│   ├── package.json
│   └── README.md
└── README.md
```

## Setup Instructions

### Laravel Backend
1. Navigate to the `backend` directory:
   ```bash
   cd backend
   ```
2. Install the dependencies:
   ```bash
   composer install
   ```
3. Copy the example environment file and configure it:
   ```bash
   cp .env.example .env
   php artisan key:generate
   ```
4. Set up the database configuration in the `.env` file.
5. Run the migrations:
   ```bash
   php artisan migrate
   ```
6. Start the server:
   ```bash
   php artisan serve
   ```

### React Frontend
1. Navigate to the `frontend` directory:
   ```bash
   cd frontend
   ```
2. Install the dependencies:
   ```bash
   npm install
   ```
3. Start the development server:
   ```bash
   npm start
   ```

## Database Configuration
- Ensure you have a MySQL database set up and modify the following in your `.env` file (in the `backend` directory):
   ```plaintext
   DB_CONNECTION=mysql
   DB_HOST=127.0.0.1
   DB_PORT=3306
   DB_DATABASE=your_database_name
   DB_USERNAME=your_database_user
   DB_PASSWORD=your_database_password
   ```

## Project Features
- User authentication (registration, login, logout)
- Browse and search for food items
- Add items to cart
- Checkout process with payment integration
- Order history tracking
- Admin panel for managing food items and orders

For more details, refer to respective documentation in the `backend` and `frontend` folders.