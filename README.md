# Maven Docker Example

    https://spring.io/guides/gs/maven/

## Prepare

    mvn compile
    mvn package
    mvn install
    mvn test

    java -jar target/gs-maven-0.1.0.jar

## Docker

    docker run -it --rm --name my-maven-project -v "$PWD":/usr/src/mymaven -w /usr/src/mymaven maven:3.2-jdk-7 mvn compile
    docker run -it --rm --name my-java-project -v "$PWD":/code -w /code java:8-jdk-alpine java -jar target/gs-maven-0.1.0.jar

## Docker compose

    docker-compose up -d maven
    docker-compose exec maven mvn -v

    docker-compose exec maven mvn compile

    docker-compose up -d java
    docker-compose exec maven java --jar target/gs-maven-0.1.0.jar

## Docker shortcuts

    sh scripts/mvm
    sh scripts/java
