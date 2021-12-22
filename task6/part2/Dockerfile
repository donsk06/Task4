FROM openjdk:8

COPY wait-for-it.sh /var/tmp

COPY /DostavimVse /var/DostavimVse

WORKDIR /var/DostavimVse

RUN ./mvnw -Pinit-base -DskipTests clean package

ENTRYPOINT /var/tmp/wait-for-it.sh -t 30 db:3306 -- java -jar target/dostavimvse-0.0.1-SNAPSHOT.jar && ./mvnw clean package -P web-app && java -jar target/dostavimvse-0.0.1-SNAPSHOT.jar