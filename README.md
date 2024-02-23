# Asp.Net Core API (5.0) - Token-Based Authentication (JWT)

This project aims to create an API using Asp.Net Core 5.0 and implement token-based authentication using JSON Web Tokens (JWT).

## Getting Started

Follow the steps below to get the project up and running.

### Prerequisites

- [.NET Core SDK 5.0](https://dotnet.microsoft.com/download/dotnet/5.0)

### Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/user/step-by-step-web-api.git
    cd step-by-step-web-api
    ```

2. Restore and build the project files:

    ```bash
    dotnet restore
    dotnet build
    ```

3. Run the application:

    ```bash
    dotnet run
    ```

## Token-Based Authentication

In this project, a simple authentication mechanism has been set up using JSON Web Tokens (JWT). Users can register, log in, and obtain a token.

### API Endpoints

- **POST /api/auth/register**: Create a new user registration.

    Example Usage:

    ```bash
    curl -X POST -H "Content-Type: application/json" -d '{"username": "user", "password": "password123"}' http://localhost:5000/api/auth/register
    ```

- **POST /api/auth/login**: Log in with an existing user and obtain a JWT.

    Example Usage:

    ```bash
    curl -X POST -H "Content-Type: application/json" -d '{"username": "user", "password": "password123"}' http://localhost:5000/api/auth/login
    ```

- **GET /api/protected**: An example endpoint requiring token authentication.

    Example Usage:

    ```bash
    curl -H "Authorization: Bearer <TOKEN>" http://localhost:5000/api/protected
    ```
