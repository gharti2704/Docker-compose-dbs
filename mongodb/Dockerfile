# Use the official MongoDB image as the base image
FROM mongo:latest

# Set the working directory inside the container
WORKDIR /usr/src/app

# Copy the MongoDB configuration file to the container
COPY mongod.conf /etc/mongod.conf

# Expose the default MongoDB port
EXPOSE 27017

# Set environment variables for username, password, and database name
ENV MONGO_INITDB_ROOT_USERNAME=admin
ENV MONGO_INITDB_ROOT_PASSWORD=secret
ENV MONGO_INITDB_DATABASE=mydatabase

# Start the MongoDB service when the container is run
CMD ["mongod", "--auth", "--config", "/etc/mongod.conf"]