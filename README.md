# E-Commerce Backend

This repository contains the backend services for an e-commerce application. It includes multiple microservices built using Spring Boot and Spring Cloud. The main components are:

- **Eureka Server**: Service discovery server.
- **Auth Service**: Handles user authentication and registration.

## Project Structure
```
The repository is structured as follows:
e-commerce-backend/
├── eureka-server/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/
│   │   │   │   └── com.example.eurekaserver/
│   │   │   │       └── EurekaServerApplication.java
│   │   │   └── resources/
│   │   │       └── application.properties
│   │   └── test/
│   │       └── java/
│   │           └── com.example.eurekaserver/
│   │               └── EurekaServerApplicationTests.java
│   └── pom.xml
├── auth-service/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/
│   │   │   │   └── com.example.authservice/
│   │   │   │       ├── AuthController.java
│   │   │   │       ├── AuthService.java
│   │   │   │       ├── AuthApplication.java
│   │   │   │       ├── model/
│   │   │   │       │   └── User.java
│   │   │   │       ├── repository/
│   │   │   │       │   └── UserRepository.java
│   │   │   │       └── security/
│   │   │   │           ├── JwtTokenProvider.java
│   │   │   │           └── WebSecurityConfig.java
│   │   │   └── resources/
│   │   │       └── application.properties
│   │   └── test/
│   │       └── java/
│   │           └── com.example.authservice/
│   │               └── AuthApplicationTests.java
│   └── pom.xml
└── README.md


```

## Getting Started

### Prerequisites

- **Java Development Kit (JDK)**: JDK 11 or higher.
- **STS4**: Spring Tool Suite 4 or any other IDE that supports Spring Boot.
- **Maven**: Ensure Maven is installed and configured.
- **Database**: PostgreSQL or any other database of your choice.
- **Git**: Ensure Git is installed.

### Setting Up the Eureka Server

1. **Navigate to the Eureka Server Directory**:
   ```sh
   cd e-commerce-backend/eureka-server



**Build and Run the Eureka Server**:
```sh

mvn clean install
mvn spring-boot:run
```
**Verify the Eureka Server**:
Open your browser and navigate to http://localhost:8761.
You should see the Eureka dashboard.
Setting Up the Auth Service
Navigate to the Auth Service Directory:
sh
Copy
cd e-commerce-backend/auth-service
Build and Run the Auth Service:
sh
Copy
mvn clean install
mvn spring-boot:run
Verify the Auth Service:
Use a tool like Postman to test the authentication endpoints.
Example endpoint: POST http://localhost:8081/api/auth/login
Configuration
Database Configuration
Ensure your application.properties files are correctly configured to connect to your database. For PostgreSQL, your application.properties should look like this:
properties
Copy
# Eureka Server
server.port=8761
eureka.client.register-with-eureka=false
eureka.client.fetch-registry=false

# Auth Service
server.port=8081
spring.datasource.url=jdbc:postgresql://localhost:5432/authdb
spring.datasource.username=authuser
spring.datasource.password=yourpassword
spring.datasource.driver-class-name=org.postgresql.Driver

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.PostgreSQLDialect

eureka.client.service-url.defaultZone=http://localhost:8761/eureka/

jwt.secret=yourSecretKey
jwt.expiration=3600000
Dependencies
Ensure your pom.xml files include the necessary dependencies for Spring Boot, Spring Cloud, and other required libraries.
Contributing
Feel free to contribute to this project by submitting pull requests. Please ensure that your contributions follow the existing code style and include necessary tests.
License
This project is licensed under the MIT License - see the LICENSE file for details.
Contact
For any questions or issues, please contact your-email@example.com.



