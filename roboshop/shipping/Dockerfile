FROM maven:3.8.5-openjdk-11 AS build
WORKDIR /app
COPY pom.xml .
RUN mvn dependency:go-offline
COPY src /app/src
RUN mvn package

FROM openjdk:24-slim
WORKDIR /app
COPY --from=build /app/target/shipping-1.0.jar /app/shipping.jar
EXPOSE 8080
ENTRYPOINT ["java", "-jar", "/app/shipping.jar"]
