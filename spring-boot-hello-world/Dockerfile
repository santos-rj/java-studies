FROM maven:3.9-eclipse-temurin-23

WORKDIR /usr/app

COPY pom.xml .
RUN mvn dependency:resolve

COPY . .

RUN mvn clean install

EXPOSE 8080

CMD ["java", "-jar", "target/hello.world-0.0.1-SNAPSHOT.jar"]
