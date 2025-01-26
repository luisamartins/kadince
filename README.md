# Kadince

Kadince Assignment

## Overview

This project consists of two main modules: `task-service` (backend) and `web-portal` (frontend). The `task-service` is a backend service developed in Java with Spring Boot, while the `web-portal` is a frontend developed in Angular.

## Project Structure

```
.gitmodules
.idea/
README.md
task-service/
web-portal/
web-portal.iml
```

### task-service

The `task-service` module contains the backend code of the project.

- **Important Directories and Files:**
  - `src/main/java/com/kadince/task/`: Contains the main backend classes.
    - [`TaskApplication`](task-service/src/main/java/com/kadince/task/TaskApplication.java): Main class to start the Spring Boot application.
    - [`TaskController`](task-service/src/main/java/com/kadince/task/controller/TaskController.java): REST controller for managing tasks.
    - [`TaskService`](task-service/src/main/java/com/kadince/task/service/TaskService.java): Service for business logic.
    - [`TaskRepository`](task-service/src/main/java/com/kadince/task/repository/TaskRepository.java): JPA repository for database access.
    - [`Task`](task-service/src/main/java/com/kadince/task/entity/Task.java): JPA entity representing a task.
  - `src/main/resources/`: Contains configuration files and SQL scripts.
    - [`application.properties`](task-service/src/main/resources/application.properties): Application configurations.
    - `db/migration/`: Database migration scripts.
  - `build.gradle`: Gradle build script.
  - `Dockerfile`: Dockerfile for containerizing the service.

### web-portal

The `web-portal` module contains the frontend code of the project.

- **Important Directories and Files:**
  - `src/app/`: Contains Angular components and services.
    - [`task.component.ts`](web-portal/src/app/task/task.component.ts): Main component for managing tasks.
    - [`task.service.ts`](web-portal/src/app/services/task.service.ts): Service for communication with the backend.
    - [`calendar-view.component.ts`](web-portal/src/app/calendar-view/calendar-view.component.ts): Component for viewing tasks in a calendar.
  - `angular.json`: Angular CLI configurations.
  - `package.json`: npm dependencies and scripts.

## Environment Setup

### Prerequisites

- Java 17
- Node.js and npm
- Docker (optional, for containerization)

### Cloning the Repository

```sh
git clone https://github.com/luisamartins/kadince.git
cd kadince
git submodule update --init --recursive
```

## Build Instructions

### Backend (task-service)

1. Navigate to the `task-service` directory:
   ```sh
   cd task-service
   ```

2. Build the project using Gradle:
   ```sh
   ./gradlew build
   ```

### Frontend (web-portal)

1. Navigate to the `web-portal` directory:
   ```sh
   cd web-portal
   ```

2. Install npm dependencies:
   ```sh
   npm install
   ```

3. Build the Angular project:
   ```sh
   npm run build
   ```

## Running the Project

### Backend (task-service)

1. Navigate to the `task-service` directory:
   ```sh
   cd task-service
   ```

2. Run the Spring Boot application:
   ```sh
   ./gradlew bootRun
   ```

### Frontend (web-portal)

1. Navigate to the `web-portal` directory:
   ```sh
   cd web-portal
   ```

2. Start the Angular development server:
   ```sh
   npm start
   ```

3. Access the application at `http://localhost:4200`.

## Testing

### Backend (task-service)

1. Navigate to the `task-service` directory:
   ```sh
   cd task-service
   ```

2. Run the tests:
   ```sh
   ./gradlew test
   ```

## API Endpoints

### `GET /api/tasks`

Returns all tasks.

### `POST /api/tasks`

Creates a new task.

### `PUT /api/tasks/{id}`

Updates an existing task.

### `DELETE /api/tasks/{id}`

Deletes a task.

## Frontend Components

### TaskComponent

Main component for managing tasks.

### CalendarViewComponent

Component for viewing tasks in a calendar.

### TaskService

Service for communication with the backend.

---

This documentation provides an overview of the project, including the code structure, build instructions, running and testing the project. For more details, refer to the mentioned code and configuration files.
