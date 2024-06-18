# Description: Dockerfile for the database container.
FROM postgres:14.1-alpine

# Copy the SQL files to the container
COPY ./data/* /docker-entrypoint-initdb.d/

# Set the environment variables
ENV POSTGRES_DB=db \
   POSTGRES_USER=usr \
   POSTGRES_PASSWORD=pwd
