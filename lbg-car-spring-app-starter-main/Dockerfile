FROM maven:latest

# change into a folder called /app
WORKDIR /app

# using maven for project management
COPY . .

RUN mvn clean package -Dmaven.test.skip

# second stage
FROM ubuntu/jre:17-22.04_edge

CMD [ "-jar", "target/cardatabase-0.0.1-SNAPSHOT.jar" ]