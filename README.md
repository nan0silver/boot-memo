# 📝 Spring Boot Memo Application

A simple memo application built with Spring Boot that allows users to create, read, update, and delete memos.

## 💡 Key Features

- ✏️ Create new memos
- 📄 View all memos
- 🔄 Update existing memos
- 🗑️ Delete individual memos or all memos at once
- 💅 Modern and responsive user interface

## 🛠️ Technology Stack

- **Backend**: Java 17, Spring Boot 3
- **Database**: PostgreSQL with MyBatis
- **Frontend**: Thymeleaf, HTML/CSS
- **Build Tool**: Gradle
- **Containerization**: Docker
- **CI/CD**: GitHub Actions

## 📁 Project Structure

```
src
└── main
    ├── java
    │   └── org.example.bootsecurity
    │       ├── controller     # Web controllers for handling HTTP requests
    │       ├── model          # Domain models and data access objects
    │       │   ├── domain     # Entity and form classes
    │       │   └── mapper     # MyBatis mapper interfaces
    │       └── service        # Business logic services
    └── resources
        ├── templates      # Thymeleaf templates
        ├── static         # Static resources (CSS, JavaScript)
        └── application.yml # Application configuration
```

## 🚀 Getting Started

### Prerequisites

- Java 17 or higher
- PostgreSQL database
- Gradle

### Running Locally

1. Clone the repository
2. Configure your database connection in `application-dev.yml`
3. Run the application:
   ```
   ./gradlew bootRun
   ```

### Docker Deployment

The project includes a Dockerfile for containerized deployment:

```bash
# Build the Docker image
docker build -t memo-app .

# Run the container
docker run -p 8080:8080 memo-app
```

## 🔄 CI/CD Pipeline

This project uses GitHub Actions for continuous integration and deployment:

- Automatic Docker image building on push to main branch
- Image publication to GitHub Container Registry
- Layer caching for faster builds