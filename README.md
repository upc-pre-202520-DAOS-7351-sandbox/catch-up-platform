# Catch-Up Platform (cath-up-platform)

## Overview

Catch-Up Platform is a small Spring Boot service that provides an API to manage users' favorite news sources. The project demonstrates a clean package structure separated into bounded contexts (news and shared) and follows simple command/query service patterns with JPA persistence.

## Features

- List favorite sources scoped to a News API key
- Retrieve a favorite source by its identifier
- Retrieve a favorite source by News API key + source id
- Create (persist) a new favorite source
- Custom Hibernate naming strategy to convert identifiers to snake_case and plural table names.

## Technologies

- Java 25+ and Spring Boot
- Spring Web (REST controllers)
- Spring Data JPA (Hibernate)
- Lombok (compile-time helpers)
- PlantUML (architecture diagrams in `docs/`)

## Technical stories

The API-focused technical stories for frontend integration are in [`docs/user-stories.md`](docs/user-stories.md).

## Class diagram

A PlantUML class diagram that reflects the code structure and bounded contexts is available at [`docs/class-diagram.puml`](docs/class-diagram.puml).

## Getting started (quick)

To run the application locally (recommended: macOS / Linux):

```bash
./mvnw spring-boot:run
```

Or build and run the jar:

```bash
./mvnw clean package
java -jar target/*.jar
```

## Notes

- This repository intentionally reflects a focused subset of functionality (favorites management). Delete operations are not currently implemented in the controllers.
- For API integration details and acceptance criteria, see `docs/user-stories.md`.
- For the system class diagram, see `docs/class-diagram.puml`.
