### Build The Project

To build this project, you will need to have the following installed:

* ```Docker & docker compose```

To build the project, follow these steps:

1. Clone the repository
2. Run the following command in the root directory of the project:

```bash
docker-compose up
```

3. The project will be built and the server will be started on port 7000 by default. To access the server, navigate
   to ```http://localhost:7000``` in your browser.

### About The Project

This project contains 3 services which are :

1. **Backend Service**: This service is responsible for handling the backend logic of the application. It is built using
   Springboot & Java. It is responsible for handling the API requests and interacting with the database.
2. **Database Service**: This service is responsible for handling the database operations. It is built using PostgreSQL relational database.
3. **Reverse Proxy Service**: This service is responsible for routing the requests to the appropriate service. It is built using Apache Server.
4. **Frontend Service**: This service is responsible for handling the frontend logic of the application. It is built using
   Vue & Javascript. It is responsible for handling the user interface and interacting with the backend service.

### Questions answers for the task

1.Why should we run the container with a flag -e to give the environment variables?

```
We have to use the -e flag to pass the environment variables to the container. This is because the environment variables
are used to configure the container at runtime. By passing the environment variables using the -e flag, we can configure
the container to use the correct settings for the application.
```

2.When we talk about /docker-entrypoint-initdb.d it means inside the container, so you have to copy your directory's content and the container’s directory.

```
docker-entrypoint-initdb.d is used to initialize the database when the container is started. The scripts in this directory
are executed when the container is started, and they are used to create the database schema and populate the database with
data.
```

3.Why do we need a volume to be attached to our postgres container?
```
We need to attach a volume to the postgres container to persist the data. When the container is stopped or removed, the data
stored in the container is lost. By attaching a volume to the container, we can store the data on the host machine, and the
data will persist even if the container is stopped or removed.
```

4.Why do we need a multistage build?
```
We need a multistage build to reduce the size of the final image. In a multistage build, we use multiple stages to build the
application, and we only copy the necessary files from the previous stages to the final stage. This allows us to reduce the
size of the final image by only including the necessary files and dependencies.
```

5.Why do we need a reverse proxy?
```
We need a reverse proxy to route requests to the appropriate service. A reverse proxy can be used to load balance requests
across multiple instances of a service, route requests to different services based on the request path, and provide SSL
termination. A reverse proxy can also be used to provide additional security features such as rate limiting, request
filtering, and authentication.
```

6.Why is docker-compose so important?
```
Docker-compose is important because it allows us to define and run multi-container Docker applications. With docker-compose,
we can define the services, networks, and volumes for our application in a single file, and we can use the docker-compose
command to build, start, stop, and manage the application. Docker-compose makes it easy to define and manage complex
Docker applications, and it provides a simple and consistent way to work with Docker containers.
```

7.What ```mvn clean verify```is it supposed to do?
```
mvn clean verify is a Maven command that is used to clean the project, compile the source code, run the tests, and package
the application. The clean goal removes the target directory, which contains the compiled classes and resources. The verify
goal compiles the source code, runs the tests, and packages the application into a JAR file. The mvn clean verify command
is typically used to build and test the application before deploying it to a production environment.
```

8. Unit tests? Component tests? Integration tests?
```
Unit tests are tests that are used to test individual units or components of the application. Unit tests are typically
written by the developers and are used to test the functionality of individual classes or methods. Unit tests are fast
and isolated, and they are used to ensure that the individual units of the application work as expected.

Component tests are tests that are used to test the interactions between components of the application. Component tests
are used to test the integration of multiple units or components and to ensure that the components work together correctly.
Component tests are slower and more complex than unit tests, but they are useful for testing the interactions between
components.

Integration tests are tests that are used to test the integration of the application with external systems or services.
Integration tests are used to test the end-to-end functionality of the application and to ensure that the application
works correctly in a production-like environment. Integration tests are slower and more complex than unit tests, but they
are useful for testing the application as a whole.
```

9. What are testcontainers?
```
Testcontainers is a Java library that provides lightweight, throwaway instances of Docker containers for testing. Testcontainers
allows developers to easily create and manage Docker containers in their tests, and it provides a simple and consistent way
to test applications that interact with external systems or services. Testcontainers can be used to test databases, message
brokers, web services, and other external systems, and it provides a convenient way to test the application in a production-like
environment.
```

10. Secured Variables in Github, why?
```
Securing variables in Github is important to prevent sensitive information from being exposed. If sensitive variables such as
API keys, passwords, or access tokens are stored in the repository, they can be accessed by unauthorized users and used to
compromise the security of the application. By securing variables in Github, we can prevent sensitive information from being
exposed and ensure that the application is secure.
```


### Documentation

Every file in the project is documented with comments to explain the purpose of the file and the code. The code is also
written in a clean and readable format to make it easy to understand and maintain.

### Accessing the application

To access the application on cloud, navigate to ```http://noreddinelamamra.takima.cloud``` in your browser (If the EC2 instance is still running).
