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
Below is an overview of the key files and folders in this API project:
```
├── app.py # Flask application entry point
├── blocklist.py # JWT token blacklist logic
├── db.py # Database connection and initialization
├── Dockerfile # Docker build configuration
├── docker-compose.yml # Docker multi-service configuration
├── docker-entrypoint.sh # Docker startup script
├── README.md # Project documentation
├── requirements.txt # Python dependencies
├── CONTRIBUTING.md # Contribution guidelines
├── schemas.py # Marshmallow schemas
│
├── migrations/ # Alembic database migrations
│ ├── versions/ # Auto-generated migration scripts
│ ├── alembic.ini
│ ├── env.py
│ └── script.py.mako
│
├── models/ # SQLAlchemy database models
│ ├── init.py
│ ├── item.py
│ ├── item_tag.py
│ ├── store.py
│ ├── tag.py
│ └── user.py
│
├── resources/ # Flask-Smorest Blueprints for API routes
│ ├── item.py
│ ├── store.py
│ ├── tag.py
│ └── user.py
```
## API Documentation

Below are screenshots showcasing the API in action:

### Swagger UI

This auto-generated documentation allows users to test endpoints interactively.

![Swagger UI Screenshot](docs/swagger-ui.png)
![Swagger UI Screenshot](docs/swagger-ui2.png)

### Insomnia Testing

Testing REST endpoints with Insomnia to verify authentication and CRUD operations.

![Insomnia Testing Screenshot](docs/insomnia-testing.png)