# Mindmap Backend API - Spring Boot with JWT

TODO - Add description

## Configure Spring Datasource, JPA, App properties
Open `src/main/resources/application-postgress.properties`

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/mindmap
spring.datasource.username=postgres
spring.datasource.password=1234

spring.jpa.properties.hibernate.jdbc.lob.non_contextual_creation=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.PostgreSQLDialect

# Hibernate ddl auto (create, create-drop, validate, update)
spring.jpa.hibernate.ddl-auto= update

# App Properties
mindmap.app.jwtSecret= bezKoderSecretKey
mindmap.app.jwtExpirationMs= 3600000
mindmap.app.jwtRefreshExpirationMs= 86400000
```
## Run MySQL 8
```
docker run --name some-mysql -e MYSQL_ROOT_PASSWORD=123456 -d mysql:latest
```

## Run Spring Boot application
```
mvn spring-boot:run
```

## Run following SQL insert statements
```
INSERT INTO ROLES VALUES(1, 'ROLE_USER', CURRENT_TIMESTAMP());
INSERT INTO ROLES VALUES(2, 'ROLE_MODERATOR', CURRENT_TIMESTAMP());
INSERT INTO ROLES VALUES(3, 'ROLE_ADMIN', CURRENT_TIMESTAMP());
```