# Spring Boot Multi-Module Template (Backend / Frontend / DTO)

## Project Goal

This project is a **Spring Boot Maven multi-module template** designed to be **cloned and reused as a project base**.

It is intended for any project using:
- a **Spring Boot backend exposing REST APIs** (mandatory),
- a **Spring Boot frontend** consuming those APIs (optional),
- a **shared DTO module** between backend and frontend (optional).

Each module can be kept, modified, or removed depending on project needs.

---

## Project Architecture

- template-parent
- template-backend → Spring Boot Backend (REST APIs)
- template-frontend → Spring Boot Frontend (optional)
- dto → Shared DTOs (optional)
- pom.xml → Maven parent (dependency & module management)

---

## Technologies

- Java 21
- Spring Boot 3.3.5
- Maven (multi-module)
- Spring Web
- Spring Data JPA
- H2 (default)
- MySQL (optional)

---

## Prerequisites

- Java JDK 21
- Maven 3.9+
- Git
- MySQL (only if used)

---

## Installation and Usage

```bash
# 1. Clone the template
git clone https://github.com/YOUR_ACCOUNT/YOUR_REPOSITORY.git
cd template-parent

# 2. Detach the template to start a new project
git remote remove origin

# 3. Maven build (parent + modules)
mvn clean install

# 4. Run the backend
cd template-backend
mvn spring-boot:run

# 5. (Optional) Run the frontend in another terminal
cd template-frontend
mvn spring-boot:run
```

## Best Practices After Cloning
1. Rename groupId / artifactId
2. Rename Java packages
3. Adjust ports if needed
4. Add tests
5. Remove unused modules
6. Start your project
   
## Default Ports
- Backend: `8080`
- Frontend: `8081`


## Database Configuration
### H2 (default)
Accessible at: `http://localhost:8080/h2-console`
JDBC URL: `jdbc:h2:mem:testdb`
### MySQL (optional)
Uncomment and configure in `application.properties`:

## Resources
- [Spring Boot Documentation](https://spring.io/projects/spring-boot)
- [Maven Guide](https://maven.apache.org/guides/)

## License
This project is licensed under the MIT License.

Free to use as a project template.





