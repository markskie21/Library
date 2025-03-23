# SPCC Library Management System

A web-based library management system for SPCC that allows users to search, borrow, and return books, and administrators to manage the library's resources.

## Features

- User authentication (admin and regular users)
- Book search and borrowing
- Excel file import for bulk book addition
- Admin dashboard for managing users, books, and settings
- Profile management with optional profile picture
- Responsive design for all devices

## Requirements

- PHP 7.4 or higher
- MySQL 5.7 or higher
- Composer
- XAMPP (recommended for local development)

## Installation

1. Clone the repository to your local machine:
```bash
git clone <repository-url>
```

2. Set up your web server (XAMPP recommended):
   - Copy the `FRONT PAGE` folder to `C:/xampp/htdocs/FRONT PAGE/`
   - Copy the `backend` folder to `C:/xampp/htdocs/backend/`

3. Install PHP dependencies:
```bash
cd backend
composer install
```

4. Create the database:
   - Open phpMyAdmin (http://localhost/phpmyadmin)
   - Import the `backend/database.sql` file

5. Configure the database connection:
   - Open `backend/config.php`
   - Update the database credentials if needed

## Default Admin Account

- Username: admin
- Password: admin123

## Directory Structure

```
├── FRONT PAGE/           # Frontend files
│   ├── frontpage.html   # Main page
│   ├── borrow.html      # Book borrowing page
│   ├── admin.html       # Admin dashboard
│   └── assets/         # Images, CSS, JS files
└── backend/            # Backend files
    ├── config.php      # Database configuration
    ├── database.sql    # Database schema
    ├── composer.json   # PHP dependencies
    └── *.php          # API endpoints
```

## API Endpoints

### Authentication
- POST /backend/login.php - User login
- POST /backend/register.php - User registration
- POST /backend/logout.php - User logout

### Books
- GET /backend/get_books.php - Get all books
- POST /backend/add_book.php - Add a new book
- POST /backend/edit_book.php - Edit a book
- POST /backend/delete_book.php - Delete a book
- POST /backend/import_books.php - Import books from Excel

### Users
- GET /backend/get_users.php - Get all users
- POST /backend/add_admin.php - Add a new admin
- POST /backend/edit_user.php - Edit a user
- POST /backend/delete_user.php - Delete a user

### Borrowings
- GET /backend/get_borrowings.php - Get all borrowings
- POST /backend/update_borrowing.php - Update borrowing status

### Settings
- GET /backend/get_settings.php - Get library settings
- POST /backend/update_settings.php - Update library settings

## Excel Import Format

When importing books from Excel, use the following column format:
1. Title
2. Author
3. ISBN
4. Category (optional)
5. Quantity (optional, defaults to 1)
6. Location (optional)

## Security Notes

- Change the default admin password after first login
- Keep your database credentials secure
- Regularly backup your database
- Update dependencies regularly

## Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a new Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details. 