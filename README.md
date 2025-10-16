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



### Feel free to contribute to this project by submitting pull requests. Please ensure that your contributions follow the existing code style and include necessary tests.
# License
This project is licensed under the MIT License - see the LICENSE file for details.
Contact
For any questions or issues, please contact imrajeevnayan@gmail.com.



