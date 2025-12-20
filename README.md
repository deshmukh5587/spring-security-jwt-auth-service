# Spring Security JWT Authentication Service

This project is a **JWT-based authentication and authorization service** built using **Spring Boot and Spring Security**.  
It secures REST APIs using **stateless authentication**, which is widely used in real-world backend applications.

## Project Objective

To design and implement a **secure backend authentication system** that supports:

- User registration  
- User login  
- JWT token-based authorization  
- Role-based access control

## Key Features

- User Signup and Login APIs  
- JWT token generation on successful authentication  
- JWT validation using a custom security filter  
- Stateless authentication (no server-side session)  
- Role-based authorization (`ROLE_USER`, `ROLE_ADMIN`)  
- Password encryption using BCrypt  
- Secure REST API design  

## Project Architecture

**Flow:**

1. User sends login request with credentials  
2. Server validates credentials  
3. JWT token is generated and returned  
4. Client sends JWT token in `Authorization` header  
5. Spring Security filter validates token on every request  
6. Authorized user can access protected APIs  

## Technologies Used

- Java  
- Spring Boot  
- Spring Security  
- JWT (JSON Web Token)  
- Spring Data JPA  
- MySQL / PostgreSQL  
- Maven  

## 📂 Project Structure

src/main/java
├── controller → REST APIs
├── security → JWT & Spring Security configuration
├── service → Business logic
├── repository → Database access
├── model/entity → JPA entities
└── dto → Request & response objects


## 🔑 API Endpoints

| Method | Endpoint        | Description            |
|--------|----------------|------------------------|
| POST   | /api/auth/signup | Register new user      |
| POST   | /api/auth/signin | User login & JWT token |
| GET    | /api/test/user  | Protected user API     |
| GET    | /api/test/admin | Admin-only API         |

## ⚙️ How to Run the Project

1. Configure database in `application.properties` (MySQL / PostgreSQL)  

2. Insert default roles into database:


INSERT INTO roles(name) VALUES('ROLE_USER');
INSERT INTO roles(name) VALUES('ROLE_ADMIN');

mvn spring-boot:run

📚 What I Learned from This Project

1. How Spring Security filter chain works
2. Difference between authentication and authorization
3. Implementing JWT-based stateless security
4. Securing REST APIs in real-world applications
5. Using JPA for database interaction
6. Writing clean, layered backend code

🔮 Future Improvements

1. Refresh token implementation
2. Swagger API documentation
3. Unit and integration testing
4. Frontend integration (React / Angular)
5. Dockerization for deployment






