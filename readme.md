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
