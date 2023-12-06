# Demo Spring Boot 3.2.0 with Docker Compose
* MySQL

## Config project
application.properties
```
spring.mvc.throw-exception-if-no-handler-found=true
spring.jackson.deserialization.FAIL_ON_UNKNOWN_PROPERTIES=true
spring.jackson.property-naming-strategy=SNAKE_CASE

spring.docker.compose.enabled=true

spring.datasource.url=${MYSQL_URL:jdbc:mysql://localhost:3306/demo_workshop?allowPublicKeyRetrieval=true&useSSL=false}
spring.datasource.username=${MYSQL_USER:user}
spring.datasource.password=${MYSQL_PASS:password}
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

## Start proejct
```
./mvnw spring-boot:run

o.s.boot.docker.compose.core.DockerCli   :  Container demo_compose-mysql-1  Created
o.s.boot.docker.compose.core.DockerCli   :  Container demo_compose-mysql-1  Starting
o.s.boot.docker.compose.core.DockerCli   :  Container demo_compose-mysql-1  Started
o.s.boot.docker.compose.core.DockerCli   :  Container demo_compose-mysql-1  Waiting
o.s.boot.docker.compose.core.DockerCli   :  Container demo_compose-mysql-1  Healthy
```
