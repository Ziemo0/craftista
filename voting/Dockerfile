FROM maven:latest AS build

WORKDIR /app

COPY . /app/

RUN mvn clean package -DskipTests

FROM eclipse-temurin:21-jre

COPY --from=build /app/target/voting-0.0.1-SNAPSHOT.jar app.jar

EXPOSE 8000

CMD ["java", "-jar", "app.jar"]
