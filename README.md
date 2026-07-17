# Classroom Management

A [Laravel](https://laravel.com/) web application for managing classroom tasks — built on Laravel 5.8 (PHP), with role/permission-based access control, PDF export, image handling, and DataTables-driven listings.

> This repository has no in-repo description, so the summary above and the feature list below are inferred from `composer.json`, `package.json`, and the folder structure. Update this section with the actual purpose/features of the app (e.g. what "tasks" represent — assignments, grading, attendance, etc.) once confirmed.

## Tech Stack

- **Backend:** PHP ^7.1.3, Laravel Framework 5.8
- **Frontend build:** Laravel Mix (Webpack), Bootstrap 4, jQuery, Vue 2, Sass
- **Database:** Laravel's default Eloquent ORM (see `database/` for migrations/seeders)
- **Deployment:** Includes a `Procfile`, suggesting deployment to a platform like Heroku

### Key packages

| Package | Purpose |
|---|---|
| `spatie/laravel-permission` | Role & permission-based access control |
| `barryvdh/laravel-dompdf` | Generating PDF documents |
| `intervention/image` | Image processing/manipulation |
| `davejamesmiller/laravel-breadcrumbs` | Breadcrumb navigation |
| `yajra/laravel-datatables-oracle` | Server-side DataTables integration |
| `tucker-eric/eloquentfilter` | Filtering Eloquent query results |

## Requirements

- PHP >= 7.1.3
- Composer
- Node.js & npm
- A database supported by Laravel (MySQL, etc.)

## Installation

```bash
git clone https://github.com/FannyDevz/Classroom-Task.git
cd Classroom-Task

# Install PHP dependencies
composer install

# Install JS dependencies
npm install

# Copy the environment file and generate an app key
cp .env.example .env
php artisan key:generate
```

Update your `.env` file with your database credentials and any other required configuration, then run the migrations:

```bash
php artisan migrate --seed
```

Build the frontend assets:

```bash
npm run dev
# or for production
npm run prod
```

## Running the App

Start the local development server:

```bash
php artisan serve
```

The app will be available at `http://localhost:8000` by default.

## Project Structure

```
.
├── app/                  # Application code (models, controllers, etc.)
├── bootstrap/            # Framework bootstrap files
├── config/                # Configuration files
├── database/              # Migrations, seeders, factories
├── public/                 # Publicly accessible entry point & assets
├── resources/views/         # Blade templates
├── routes/                    # Route definitions
├── storage/                    # Logs, compiled views, uploaded files
├── tests/                        # PHPUnit tests
├── artisan                        # Laravel CLI
├── composer.json
├── package.json
└── webpack.mix.js
```

## Testing

```bash
php artisan test
# or
vendor/bin/phpunit
```

## License

This project is built on the Laravel framework, which is open-sourced under the [MIT license](https://opensource.org/licenses/MIT). Check with the repository owner for the license terms of the application code itself, as none is specified in the repository.
