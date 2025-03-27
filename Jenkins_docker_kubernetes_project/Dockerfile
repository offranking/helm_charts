FROM maven:3.9.9-eclipse-temurin-17 AS builder
WORKDIR /app
COPY pom.xml .
COPY src ./src
RUN mvn clean package -DskipTests
FROM openjdk:17-jdk-slim
WORKDIR /app
COPY --from=builder /app/target/*.jar app.jar
EXPOSE 8081
ENTRYPOINT ["java", "-jar", "app.jar"]
# write your Docker file code here
# Step 1: Use Maven image to build the project
# FROM maven:3.9.9-eclipse-temurin-17 AS builder

# # Set the working directory inside the container
# WORKDIR /app

# # Copy the Maven project files
# COPY * .
# COPY * ./src

# # Build the application (Assuming it generates target/todo-app.jar)
# # RUN mvn clean package -DskipTests

# # Step 2: Use OpenJDK as the runtime image
# FROM openjdk:17-jdk-slim

# # Set working directory in the runtime container
# WORKDIR /app

# # Copy the built JAR file from the builder stage
# COPY --from=builder /app/*.jar app.jar

# # Expose port (Change if required)
# EXPOSE 8080

# # Command to run the application
# ENTRYPOINT ["java", "-jar", "app.jar"]