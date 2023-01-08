When downloading the code, it is necessary to add the *application.properties* in the indicated place according to the documentation

application.properties model (must be adjusted according to the machine where it will be installed):

```
#spring.jpa.hibernate.ddl-auto=updatespring.datasource.url=jdbc:mysql://111.22.333.444:9999/g6shop

#spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
#spring.datasource.driverClassName=com.mysql.jdbc.Driver
spring.datasource.username=senha
spring.datasource.password=senha

spring.jpa.open-in-view=falsespring.mvc.format.date=yyyy-MM-dd

spring.mvc.format.date-time=yyyy-MM-dd'T'hh:mm
spring.mvc.format.time=HH:mm:ss

admin.standardUserName=teste
admin.standardPassword=teste

spring.servlet.multipart.max-file-size=10MB
spring.servlet.multipart.max-request-size=10MB
```

Command to compile and run a background server:
mvn package & start java -jar target/dependency/webapp-runner.jar --port 5339 target/*.war

To compile only:
mvn package

To run a background server only:
start java -jar target/dependency/webapp-runner.jar --port 80 target/*.war

## Code coverage report:

Only the first time:

```
mvn clover:instrument
mvn clover:clover
```

On the following times:

``mvn clover:clover``

Documentation:

``mvn javadoc:javadoc``
