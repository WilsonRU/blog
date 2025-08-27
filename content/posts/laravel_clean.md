+++
title = "Laravel REST API Boilerplate with Service Layer, DTOs, and Clean Architecture"
date = 2025-08-27 19:35:00
tags = [
    "software engineer",
    "software engineering",
    "backend",
    "fullstack",
]
[extra]
reaction = false
+++

This boilerplate provides a **clean and scalable** foundation for applications built with **Laravel 12**, incorporating best practices in architecture, separation of responsibilities, and the use of **DTOs** (Data Transfer Objects).

---

## 🚀 Key Features

-   **Laravel 12** — the latest version of the framework.
-   **Service Layer** — isolation of business logic from controllers.
-   **Repository Pattern** — abstraction of persistence, facilitating testing and maintenance.
-   **Rate Limiter** — protection against abuse and brute-force attacks.
-   **DTOs (Data Transfer Objects)** — validation and standardization of data transferred between layers.
-   **Clean Architecture Principles** — ensures long-term scalability and maintainability.
-   **Laravel Sanctum with JWT** — ready-to-use REST API authentication.
-   **Laravel Pint** — automatic code formatting.
-   **PHPStan (Level 8)** — static analysis for type safety and error prevention.

---

## 📂 Project Structure

    app/
     ├── Dto/                 # Data Transfer Objects
     ├── Http/
     │    ├── Controllers/    # Controllers for requests and responses
     ├── Repositories/        # Repository interfaces and implementations
     ├── Services/            # Business logic layer
     └── Models/              # Eloquent Models

---

## 🛠 How It Works

The flow follows the pattern **Request → Controller → DTO → Service → Repository → Database**:

1.  **Controller**: receives the request and transforms the data into DTOs.
2.  **DTO**: validates and structures the data.
3.  **Service**: applies business rules.
4.  **Repository**: interacts with the database.

This keeps controllers lean and the system modular.

---

## 🔑 Authentication

The boilerplate includes authentication via **Laravel Sanctum + JWT** for REST APIs.

Example of a successful login:

```json
{
    "token": "jwt_token_here",
    "user": {
        "id": 1,
        "name": "Test"
    }
}
```

------------------------------------------------------------------------

## 🧪 Testing

-   Services and Repositories can be tested in isolation.\
-   DTOs ensure data consistency in tests.

Run tests:

``` bash
php artisan test
```

------------------------------------------------------------------------

## 🖌 Code Quality

-   **Laravel Pint**: apply code style formatting.\
-   **PHPStan Level 8**: advanced static analysis to detect issues early.

``` bash
composer pint
composer stan
```
------------------------------------------------------------------------

## 📦 Installation

``` bash
git clone https://github.com/WilsonRU/laravel-rest-boilerplate.git
cd laravel-rest-boilerplate
composer install
cp .env.example .env
php artisan key:generate
php artisan migrate
```
------------------------------------------------------------------------

## 🎯 Conclusion

The Laravel REST API Boilerplate is a solid foundation for developing modern APIs, ensuring security, scalability, and code quality.
Ideal for those looking to start projects with best practices already implemented.