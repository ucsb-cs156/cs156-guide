---
layout: default
title: "Swagger UI"
nav_order: 3
parent: "Development Tools"
grand_parent: Services
---

# Swagger UI

Swagger UI is a development tool for backend REST APIs. Swagger UI allows a service's API endpoints to be visualized, documented, and experimented with in a web browser, with minimal setup code. Developers can try out project API endpoints with custom parameters without the need to set up additional tools such as Postman, as well as document such APIs for future visitors and developers.

In CMPSC 156, Swagger UI is introduced in team01 and is tightly integrated into all team assignments and legacy code projects. Since it requires no additional setup for students, we encourage them to use Swagger UI as the primary place to test and debug backend endpoints. As Swagger UI is built and run along with our Spring Boot backend, Swagger UI is able to use the same website cookies as the running application, removing the need to manually authenticate Swagger UI endpoint calls.

## Running Swagger UI

Swagger UI is run as part of the Java Spring Boot backend. To start the backend and access Swagger UI, simply run the following command in the project's root directory:

```
mvn spring-boot:run
```

After the Spring Boot application is started, Swagger UI can be accessed by visiting the `/swagger-ui/index.html` endpoint. If a project detects that you're running on a local machine / development environment, and the application frontend is also running, a direct link to Swagger UI will also be present in the navbar of the running project.

To test authenticated endpoints, simply visit the running web application outside of Swagger UI, log in as usual, and then return to Swagger UI. Cookies from the running application should be usable within Swagger UI as both operate from the same domain.

Swagger UI is also built as part of the Heroku deploy process, even though the link is hidden from the running application. As a result, Swagger UI can be accessed from Heroku using the same endpoint as above. This can serve as a helpful tool for testing a code change's functionality in a pull request review.
