# Spring Boot Rest API secured with Oauth2 scheme
Spring boot backend application which supports User Authentication OAuth2. 
OAuth as authorization framework for REST/APIs enables application to obtain limited access data without giving away a user's password. Framework decouples authentication from authorization and supports multiple use cases. Swagger UI was also configured for requesting tokens from embedded auth server, it also inserts token to API calls and can be utilized as ready to use testing Interface with documentation support.

## How to start ?

Maven
```
$ mvn spring-boot:run
```
Linux start up
```
$ java -jar -server -XX:+UseG1GC -Xmx7g -Xms5g -Dspring.profiles.active=local -DNAME=OAUTH2-REST springboot-oauth2-res-1.0.0-SNAPSHOT.jar 2>> /dev/null >> /dev/null
```
```-Dspring.profiles.active=local``` : By using this system property it is possible to switch between application.properties and application-local.properties. Using the same file naming syntax possible to introduce several prop files

```-DNAME=OAUTH2-REST``` : It makes easier to find your microservice among server processes, there can be many microservices and you can grep your process using the name you set.

## Swagger-UI
* After starting the application Click on [Swagger-home](http://localhost:8080/api/swagger-ui.html)


## User Data

```
   user-name | password
   user1     | password
   user2     | password
```


## Authorize
* Use above given user details to login and generate the authorization token.
![Swagger-Home](/authentication/src/main/resources/images/Swagger-ui-auth.png "Swagger UI Home")

![Swagger-Home](/authentication/src/main/resources/images/swagger-ui-login.png "Swagger UI Home")

* Login using the generated token
![Swagger-Home](/authentication/src/main/resources/images/swagger-ui-login-token.png "Swagger UI Home")



## Change OAuth configuration
* Edit the configuration in the file [application.properties](/authentication/src/main/resources/application.properties)

```
server.port=8080
server.contextPath=/api

logging.level.com.alfred=DEBUG

# Data source properties
spring.jpa.hibernate.ddl-auto=validate
spring.jpa.show-sql=true

# openssl genrsa -out jwt.pem 2048
# openssl rsa -in jwt.pem
config.oauth2.privateKey=MIICXQIBAAKBgQDNQZKqTlO/+2b4ZdhqGJzGBDltb5PZmBz1ALN2YLvt341pH6i5mO1V9cX5Ty1LM70fKfnIoYUP4KCE33dPnC7LkUwE/myh1zM6m8cbL5cYFPyP099thbVxzJkjHWqywvQih/qOOjliomKbM9pxG8Z1dB26hL9dSAZuA8xExjlPmQIDAQABAoGAImnYGU3ApPOVtBf/TOqLfne+2SZX96eVU06myDY3zA4rO3DfbR7CzCLE6qPnyDAIiW0UQBs0oBDdWOnOqz5YaePZu/yrLyj6KM6Q2e9ywRDtDh3ywrSfGpjdSvvoaeL1WesBWsgWv1vFKKvES7ILFLUxKwyCRC2Lgh7aI9GGZfECQQD84m98Yrehhin3fZuRaBNIu348Ci7ZFZmrvyxAIxrV4jBjpACW0RM2BvF5oYM2gOJqIfBOVjmPwUrobYEFcHRvAkEAz8jsfmxsZVwh3Y/Y47BzhKIC5FLaads541jNjVWfrPirljyCy1n4sg3WQH2IEyap3WTP84+csCtsfNfyK7fQdwJBAJNRyobY74cupJYkW5OK4OkXKQQLHp2iosJV/Y5jpQeC3JO/gARcSmfIBbbI66q9zKjtmpPYUXI4tc3PtUEY8QsCQQCcxySyC0sKe6bNzyC+Q8AVvkxiTKWiI5idEr8duhJd589H72Zc2wkMB+a2CEGo+Y5Hjy5cvuph/pG/7Qw7sljnAkAy/feClt1mUEiAcWrHRwcQ71AoA0+21yC9VkqPNrn3w7OEg8gBqPjRlXBNb00QieNeGGSkXOoU6gFschR22Dzy

# openssl rsa -in jwt.pem -pubout
config.oauth2.publicKey=MIGfMA0GCSqGSIb3DQEBAQUAA4GNADCBiQKBgQDNQZKqTlO/+2b4ZdhqGJzGBDltb5PZmBz1ALN2YLvt341pH6i5mO1V9cX5Ty1LM70fKfnIoYUP4KCE33dPnC7LkUwE/myh1zM6m8cbL5cYFPyP099thbVxzJkjHWqywvQih/qOOjliomKbM9pxG8Z1dB26hL9dSAZuA8xExjlPmQIDAQAB


#oauth configurations
config.oauth2.tokenTimeout=3600
config.oauth2.resource.id=oauth2-resource
config.oauth2.clientID=client
config.oauth2.clientSecret=secret
security.oauth2.client.grantType=client_credentials
config.oauth2.accessTokenUri=http://localhost:8080/api/oauth/token
config.oauth2.userAuthorizationUri=http://localhost:8080/api/oauth/authorize
config.oauth2.resourceURI= http://localhost:8080/api/oauth/authorize
```










