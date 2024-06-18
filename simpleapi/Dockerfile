# Description: Dockerfile for simpleapi
FROM maven:3.8.6-amazoncorretto-17 AS myapp-build

# Declare the environment variables
ENV MYAPP_HOME /opt/myapp

# Copy the files to the container
WORKDIR $MYAPP_HOME
COPY pom.xml .
COPY src ./src

# Build the application
RUN mvn package -DskipTests

# Run
FROM amazoncorretto:17

# Declare the environment variables
ENV MYAPP_HOME /opt/myapp
WORKDIR $MYAPP_HOME

# Copy the files to the container
COPY --from=myapp-build $MYAPP_HOME/target/*.jar $MYAPP_HOME/myapp.jar

# Command to run the application
ENTRYPOINT java -jar myapp.jar
