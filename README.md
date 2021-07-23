## Evolve your Spring-Boot application with Liquibase [![Build Status](https://travis-ci.org/hhimanshu/spring-boot-liquibase.svg?branch=master)](https://travis-ci.org/hhimanshu/spring-boot-liquibase)

### Blog
https://medium.com/@harittweets/evolving-your-database-using-spring-boot-and-liquibase-844fcd7931da

### How to run?
clone the codebase
```bash
git clone git@github.com:hhimanshu/spring-boot-liquibase.git
```

compile, test, package
```bash
mvn clean package
```

run
```bash
mvn spring-boot:run
```

Go to http://localhost:8080/h2-console  
  
`JDBC URL`: jdbc:h2:mem:testdb  
`User Name`: sa  
`Password`: Leave it blank

Now you have the access of in-memory `H2` database dashboard.

Added Dependencies
The project requires the following dependencies be installed on the host machine:

Java Development Kit 8 or later
Apache Maven 3 or later
Running
The project uses Maven for build, package, and test workflow automation. The following Maven goals are the most commonly used.

spring-boot:run
The spring-boot:run Maven goal performs the following workflow steps:

compiles Java classes to the /target directory
copies all resources to the /target directory
starts an embedded Apache Tomcat server
To execute the spring-boot:run Maven goal, type the following command at a terminal prompt in the project base directory.

mvn spring-boot:run
Type ctrl-C to halt the web server.

This goal is used for local machine development and functional testing. Use the package goal for server deployment.

test
The test Maven goal performs the following workflow steps:

compiles Java classes to the /target directory
copies all resources to the /target directory
executes the unit test suites
produces unit test reports
The test Maven goal is designed to allow engineers the means to run the unit test suites against the main source code. This goal may also be used on continuous integration servers such as Jenkins, etc.

To execute the test Maven goal, type the following command at a terminal prompt in the project base directory.

mvn clean test
package
The package Maven goal performs the following workflow steps:

compiles Java classes to the /target directory
copies all resources to the /target directory
executes the unit test suites
produces unit test reports
prepares an executable JAR file in the /target directory
The package Maven goal is designed to prepare the application for distribution to server environments. The application and all dependencies are packaged into a single, executable JAR file.

To execute the package goal, type the following command at a terminal prompt in the project base directory.

mvn clean package
