FROM openjdk:16.0.1 AS hello

COPY gradlew .
COPY gradle gradle
COPY build.gradle .
COPY settings.gradle .
COPY src src

RUN chmod +x ./gradlew
RUN ./gradlew bootJar


FROM openjdk:16.0.1
ARG JAR_FILE=./build/libs/*.jar
COPY --from=hello ${JAR_FILE} app.jar
ENTRYPOINT ["java", "-jar", "/app.jar"]