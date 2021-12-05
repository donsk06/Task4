FROM openjdk:8

WORKDIR /DostavimVse

COPY DostavimVse /DostavimVse

RUN ./mvnw -Pinit-base -DskipTests clean package

CMD ["java", "-jar", "./target/dostavimvse-0.0.1-SNAPSHOT.jar"]