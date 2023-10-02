# README - Spring Boot REST API

## General Description

This application is a REST API developed in Spring Boot that provides endpoints for performing CRUD (Create, Read, Update, Delete) operations on entities such as `Author`, `Location`, and `Person`. It also implements the Hibernate Envers audit system to track revisions in the `Revision` entity.

## Folder Structure

- `com.example.springbootapirest.config`: Contains custom configuration, such as `CustomRevisionListener`, used for revision auditing.
- `com.example.springbootapirest.controllers`: Contains controllers that handle HTTP requests and responses.
- `com.example.springbootapirest.entities`: Contains entity classes like `Author`, `Location`, `Person`, etc.
- `com.example.springbootapirest.repositories`: Contains repository interfaces for the entities.
- `com.example.springbootapirest.services`: Contains service interfaces and implementations that handle business logic.
- `resources`: Contains the database configuration file (`application.properties`) and H2 console configuration (`h2-console`).

## Controllers

- `AuthorController`, `LocationController`, `PersonController`: Controllers that handle CRUD operations for the `Author`, `Location`, and `Person` entities.

## Services

- `AuthorServiceImpl`, `LocationServiceImpl`, `PersonServiceImpl`: Service implementations that perform operations on the corresponding entities.

## Audit

- `Revision`: Entity class that stores revision information such as date and time.
- `CustomRevisionListener`: Configuration class that listens to entity revisions and performs custom actions if necessary.

## Database

The application uses an in-memory H2 database with the H2 console enabled for easy debugging and development. You can access the H2 console at [http://localhost:8080/h2-console/](http://localhost:8080/h2-console/). Database configuration is located in `application.properties`.

## API Documentation

The API is documented using Springdoc OpenAPI. You can access the API documentation at [http://localhost:8080/swagger-ui/index.html](http://localhost:8080/swagger-ui/index.html) once the application is running.

## Running the Application

To run the application, you can use the `main` method in the `SpringbootApiRestApplication` class. Make sure the database is correctly configured in `application.properties` before running the application.

## Additional Notes

- The application uses Lombok annotations to automatically generate getter, setter, and other access methods in entity classes.
- Hibernate Envers is used to audit entity revisions, allowing tracking of data changes over time.

This is a high-level overview of the Spring Boot REST API application. You can explore individual classes and packages for more details on the implementation and specific functionality of each component.
