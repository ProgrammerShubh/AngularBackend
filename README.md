
# Spring Boot CRM Application

![Java Version](https://img.shields.io/badge/Java-17-blue)
![Spring Boot Version](https://img.shields.io/badge/Spring%20Boot-3.3.0-brightgreen)
![MySQL Version](https://img.shields.io/badge/MySQL-8.0-blue)

This repository contains a full-stack CRM (Customer Relationship Management) application built with Spring Boot, designed for managing customer relationships, projects, and usage monitoring.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Setup Instructions](#setup-instructions)
- [Usage](#usage)
- [Testing](#testing)
- [Contributing](#contributing)
## Introduction

The Spring Boot CRM application provides comprehensive functionality for managing users, projects, and monitoring usage. It uses Spring Boot for the backend, MySQL for data storage, and can be integrated with a frontend framework like Angular.

## Features

- **User Management:**
  - CRUD operations for managing users.
  - User details and project associations.

- **Project Management:**
  - CRUD operations for managing projects.
  - Project updates, deadlines, and payment tracking.

- **CRM Functionality:**
  - Integration with user management.
  - Linking projects to users.

- **Usage Monitoring:**
  - Logging and monitoring of application usage.
  - Tracking actions performed by users.

- **Authentication and Authorization:**
  - User authentication using Spring Security.
  - Role-based access control (Admin, Standard User).

## Prerequisites

Before you begin, ensure you have the following installed:

- Java Development Kit (JDK) 17 or higher
- Maven
- MySQL database
- Your preferred IDE (Eclipse, IntelliJ IDEA, etc.)

## Setup Instructions

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/spring-boot-crm.git
   cd spring-boot-crm
   ```

2. **Database Configuration:**

   - Create a MySQL database schema named `crm_db` (or your preferred name).

   - Configure the database connection in `src/main/resources/application.properties`:

     ```properties
     spring.datasource.url=jdbc:mysql://localhost:3306/crm_db
     spring.datasource.username=root
     spring.datasource.password=password
     spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
     spring.jpa.hibernate.ddl-auto=update
     ```

3. **Run the Application:**

   - You can run the application using Maven:

     ```bash
     mvn spring-boot:run
     ```

   - Alternatively, you can build the JAR file and run it:

     ```bash
     mvn clean package
     java -jar target/demo-0.0.1-SNAPSHOT.jar
     ```

4. **Access the Application:**

   - Once the application is running, access it at: `http://localhost:8080`

## Usage

- **API Endpoints:**
  - The application exposes RESTful API endpoints for CRUD operations on users and projects.
  - Secure endpoints are protected using Spring Security with role-based access control.

- **User Interface (UI):**
  - Integrate with an Angular frontend or use tools like Postman to interact with API endpoints directly for testing.

## Testing

- Unit tests are included under `src/test/java` using JUnit and Mockito.
- Run tests using Maven:

  ```bash
  mvn test
  ```

## Contributing

Contributions are welcome! Please fork the repository and create a pull request with your proposed changes.
