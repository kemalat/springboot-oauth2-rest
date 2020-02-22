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
* Swagger Home page 

![Swagger-Home](https://lh3.googleusercontent.com/Te67ojpRqRx6BL4e2oLPJfdFU1QrzCnpHK1LiCF6xUYxKGHGkBaMTq2aXIRJaY8svsn3YZrpZWH9h6iKR8KjcjwqfGox5lr1vabAxkuB51oMlcf1azoXwm2c8iS671Ih_9p8IffGA9-yWVjsRKjWm9GZ1zjQV1xWmOjzPpNP3XWX2ULGcLN0cIIKpE0ujg_wRA2kR8D5GfJZisOrcWYycvx84c2nWmdzEuSfXHkVmimZ5xR8INmZ8IWLHj3a2CKzMoC5rdqnhzkUFgATB0C0ZnCeRo7PfA37Fny69AAliypBjcfy-Bo7US5Fe4-n1YIRwaNU-wl1QeUmOjwfeB7-q4Q-XgqdBwk7-QkH7Uw5-1PpLlYZhPzbJ5eDq77q-iqKRhW1qUihafb5bNSrckqZ90Ht8bmOaIZwbPcYFOPppRZ1rWssdQKoem1niWIZBch__d9JvNwuSOM3UqIiupHAylSI9_PUal8UGFNPKhxBjBSTGvIreGD61LfbC4vmzWa6mQ1njZzbpr-JGPafQVc3c9JurKjIUUlSgpTrxLUz9NdtEF-KZcT5crAuaIQvfJbYTS1P1xlhviOf3t09JMfvd5bz-A4ouZk_3Ioqi4Wye_WD86xKf90ZfeSmUV5eT4nQcfRimcF3KcswLskWPys5k045t67tVtXR8XChB8RqazxYJa4LBlZpQVac1nwkxAZZwXIKLsrdfW3h99u_8OWs_THG7VgbKqXKK4Q_T6qufLq23dtW=w962-h446-no "Home")

* Login with user/password and client screet

![Login](https://lh3.googleusercontent.com/RrVJO49-s-r--DT5KigI0ozTwFOTV4gA0sleNCDxqesHxOXk5Hw67W3tkaMrvo2ya9oE2AkkCmrtvPcP7qYbykE1uk9NDp0liJuoQZCZdbWn8PKANQTf0h23p4QGChBPDaAtMr9qGSaD9tZktWipNzVBTOhQoA5l1s-sdQxkO3G9ev99NeCOUQsPXROhYzJ_m0vTAnHm2atFEhAZFuAD-ylNR_3x4HDdWOglt1E8N_ykM0vAM5Xp-U9r1RBVvp5MBLJvxtPDhymsTy9WXbP3s7TnpxLleTlUpp7LxVBdVAcua6_wNw2U7pSSXi9xDSMrhS2N4cShgjg892Wl134bWkELf47Kc-jkwN8KlmPgz8006N8qV7n_yDZb_eW6IpLMwmZKi8Yv-ZEosKhystY6osfAOk7Ytk_D5cumV02jA2qrTm9-GY1r7oJuFredPIBy9PNtYXGUHwewKcrudzNOXNaGXvvuG4MKXH1HPFilTCWms5qKcp4Qv2bqn5pzdVKqoTuITkLO8MkoewI8yB5CBOoW2CpY0nGLglb-2YmC6S7Gfoxn2ovGsowHoeLrIGut2iJvNHE20CwoSl3JFFydtV7Rco8x2Ewys6QNg9CLz7gdhaPahw6D9jbJikAZqjUUH2hChY8aw4SUYfcFEALQk6kUc2dgdi6oxTinRVULE9JQgTqjalnMRBB0SXYWFD0ycSba31njPnXfD5UxiUjFRafk5JEgxM-3Fz8Nv6l5A4-3E3PY=w732-h673-no "Login")

* Login success

![Login](https://lh3.googleusercontent.com/gZ4ezgeZwOYA1U9MVAQ08tEE4jBWtOms1qWEK-I4jNGaD_vcAWJlJhd2mDHHevQumP3-oo5P-5lO0GZZwu8O_EjS_ntiDpB61E67GgrCq9q1uuM_zUShP_57K4AzLMd80w8NK7PsasIY65ai7OUs7MraycQ2CnCA4T3eRf98JGPZ5kMjsvfxdNLJ14v2jmjx6jfnJC8_tv1MXg44gsnB1dOesZZp-7YcMWxqZgv9-iTRBbthSqzlm2I-v3FgS5mAZj_vAwLR4Ol3u4ojkXao9fcheRIRhL9sic67dPWhSc1eljQZHNzLwDZD9uFjXAMfD5ZvOnRSz7hEmwYvIv7xmTti2b6fTEKZ4kNRRCDDdsdpfCYtUvW-r6BEH4LgFYJhVSyADrFm6lc8TrHZnWzZS95FkBcYk88RVyml5IkT0Z5H6_wo_gFawmKDeKe7j7bpRKv52PgbsWDzpoSTvpm7m2VYBYLbglpWvzZwvt1fqZaAvel0WQRHRwNCErR2Mq8so-sacjxGASCspYauJTAawLph4dZf0IUq3Yn-2tqrbJ4gMSMSVq4cG1JSDamsX9CNszv1G2lngRr-K4JRCwmiLxv0ULysqJDlj5mfEWLZM7GhGU7AGgxCBgGKF_szz_YsxUNYbREJW6dk1_XBY36FEXUHozLSEetb4JQGWBV5rqUvHg13mJyvNKDWdVYLGOwzEsAMj8TZT65NHAuv79il2FMAUXH0sm_eEGYsZrRCDzpIn0Xn=w624-h484-no "Login Success")



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

## Enabling SSL for Rest endpoint

Required keytool commands to convert keystore format to pkcs12
```
keytool -import -alias tomcat -file /etc/letsencrypt/live/oriontec.de/cert.pem -keystore keystore.p12 -storepass password
keytool -importkeystore -srckeystore keystore.p12 -destkeystore keystore.p12 -deststoretype pkcs12
openssl pkcs12 -export -in fullchain.pem -inkey privkey.pem -out /opt/postmail/classes/keystore.p12 -name tomcat -CAfile chain.pem -caname root
```








