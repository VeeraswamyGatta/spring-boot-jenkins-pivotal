# tasks-angularjs-springboot
Spring Boot Application

This is a application using Spring Boot, Angular JS and H2 database embedded in-memory running in Jetty.

For access web browser H2 embedded go to http://localhost:8082 and connect to the database "jdbc:h2:mem:testdb", username "sa", password empty.


Step to running application in machine:

1 - Git clone application.

2 - Dependency install in machine Java 8 and Maven.

3 - Enter in folder and execute command line: 
``` script
mvn package.
```
4 - After execute command java:
``` script
java -jar target/tasks-angularjs-springboot-0.0.1-SNAPSHOT.jar
```
5 - Application started in port 8080.

You can access application in Paas Heroku.

The basic autenthication is:

user: user

password: xpto123

https://evening-caverns-77497.herokuapp.com

