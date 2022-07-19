FROM openjdk:16.0.1

ARG JAR_FILE=./build/libs/slf4j-logback-lab-0.0.1-SNAPSHOT.jar

ADD ${JAR_FILE} app.jar

EXPOSE 8080

ENTRYPOINT ["java", "-jar", "/app.jar"]