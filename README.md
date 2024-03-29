# JWT Authentication with Spring Boot’s inbuilt OAuth2 Resource Server

**This repo hosts the source code corresponding to the article [JWT Authentication with Spring Boot’s inbuilt OAuth2 Resource Server](https://loneidealist.medium.com/stateless-jwt-authentication-with-spring-boot-a-better-approach-1f5dbae6c30f)**.

This example project demonstrates the usage of Spring Boot OAuth2 Resource Server
with JWT configuration to protect a REST API with JWT based authentication.

Furthermore, provides a "/login" endpoint to generate and issue JWTs upon
successful login by the users.

This approach is ideal to be used as the 
**backend for a single page application (SPA)** written using a frontend framework like
ReactJS, Angular, etc...

**Note:** A sample implementation of a ReactJs app is included in the `frontend` directory.

## Solution Overview

![Solution Overview](https://github.com/IMS94/spring-boot-jwt-authentication/blob/master/solution_overview.png?raw=true "Solution Overview")

## Getting Started

- Use `./mvnw clean install` in the project root directory to build the project. 
- Run the main class, `com.example.springboot.jwt.JwtApplication` to start the application.

### Sample ReactJs App

- A sample ReactJs app to consume the created API is located in `frontend` directory. Simply run `npm install` and `npm start` within that to start the app.

## Endpoints

- `/login` -> Public endpoint which returns a signed JWT for valid user credentials (username/password)
- `/user` -> A protected endpoint which returns the user details of the 
requesting user.

## See Also
1. See https://github.com/IMS94/spring-boot-jwt-authorization for an extension of this for **role based access control** (RBAC)
