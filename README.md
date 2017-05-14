# MAVEN Example

## Prepare

mvn compile
mvn package
mvn install
java -jar target/gs-maven-0.1.0.jar

## Docker images

docker run -it --rm --name my-maven-project -v "$PWD":/usr/src/mymaven -w /usr/src/mymaven maven:3.2-jdk-7 mvn compile
docker run -it --rm --name my-java-project -v "$PWD":/code -w /code java:8-jdk-alpine java -jar target/gs-maven-0.1.0.jar
