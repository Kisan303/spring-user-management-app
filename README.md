# Spring User Management Application

## Project Overview
This Spring Boot application is a demonstration of advanced concepts in Java programming and Spring framework. It provides user management functionalities including validation, caching, and RESTful endpoints, along with templating using Thymeleaf and modern testing practices.

## Features

### Q1: User and Occupation Classes
- **User**:
  - `String name` - Must be between 2 and 40 characters.
  - `Integer age` - Must be at least 18.
  - `Occupation occupation` - Represents the user's job.
  
- **Occupation**:
  - `String title` - The title of the occupation.
  - `Integer salary` - Must be at least 1.

### Q2: UserCache
A caching layer with the following methods:
- **Fetch user by name** (using streams).
- **Fetch all users** with at least a minimum salary and below a certain age (using streams).
- **Fetch the Occupation with the largest salary** (using streams).
- **Fetch all users**.
- **Add a new user**.

### Q3: Controllers
#### MainController:
- Injects the `UserCache` class.
- Handles:
  - `GET /users` - Returns a Thymeleaf template displaying all users.
  - `GET /create` - Displays a form to create a new user.
  - `POST /create` - Validates and saves a user or redisplays the form with errors.

#### UserRestController:
- Injects the `UserCache` class.
- Handles:
  - `GET /mostpaid` - Returns the Occupation with the highest salary.

### Q4: Templates
- **users.html**:
  - Displays all users with their ages and salaries in an HTML table.
  - Shows the Occupation with the highest salary, updated via AJAX every 2 seconds.
  
- **create.html**:
  - A form for creating a new user and their occupation.
  - Displays validation errors when necessary.

### Q5: ExamQuestions Class
Static methods to solve:
1. **Count consonants** in a string recursively.
2. **Check if a number is prime** recursively.

### Q6-Q7: Unit Tests
- **UserCache** (Q2): Validates caching logic.
- **MainController and UserRestController** (Q3, Q4): Verifies model attachments and templates.
- **ExamQuestions** (Q6, Q7): Tests recursive algorithms for correctness.

---

## How to Run the Application

### Prerequisites
- Java 17 or later
- Maven
- Spring Boot
- Thymeleaf

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/spring-user-management-app.git
   cd spring-user-management-app
