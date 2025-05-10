# Store Items REST API

A production-ready REST API built with Flask for managing users, stores, items, and tags. This project implements secure JWT-based authentication, supports background task processing, and is fully containerized using Docker and deployed on Render.

## Features

- **User Authentication**
  - Register, login, logout
  - Access and refresh tokens
  - JWT blacklisting for secure logout

- **Store Management**
  - Create, retrieve, and delete stores

- **Item Management**
  - Full CRUD operations
  - Items are tied to specific stores

- **Tag Management**
  - Categorize items with tags
  - Many-to-many relationship between tags and items

- **Background Tasks**
  - Send emails using Redis Queue (RQ)

- **Documentation & Testing**
  - Swagger UI for live API documentation
  - Insomnia/Postman for endpoint testing

## Tech Stack

- **Backend:** Flask, Flask-Smorest
- **Authentication:** Flask-JWT-Extended
- **Database:** PostgreSQL, SQLAlchemy, Flask-Migrate
- **Serialization & Validation:** Marshmallow
- **Containerization:** Docker, Docker Compose
- **Task Queue:** Redis Queue (RQ)
- **Deployment:** Render.com
- **Version Control:** Git & GitHub

## Project Structure

