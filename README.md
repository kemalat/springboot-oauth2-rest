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

![Login](https://lh3.googleusercontent.com/NRvng_HHtzZvesxFdXttMsSxMz3BC0TlIABJku3fEMf4VpiBo-Gy4I21h3LTg6Xq-Ild0QKzze0lQOBC688tzkhPdENnqtwY1Z8oxshrwm2Tl9P_6_xsfHYT6WrUXCvVb_bm67V3LCLHAPLNXOYi6zGdUQpqCKgK-1XmGqNoEtqH1w_oOxgsIwF7r9VOLQ2vlR1DdFRU0r7voOww9ij-dW9Yb-4BVVgioVBtM0yj8_ytiqS4LKj1Y7_kSq49xt9KXR3HTXiNMPK_Uvyc1DVlWWdcBuKEbd6yjzp-g7p9V213hUhzKw0CGVmdxRGO9EPtuqfbdmMBSoYOH7Rnj3tNJV5WwtvrYCNrd7NmZu3CRKSVmjNsDk7ZXlNWhu0YMNpzVKAIHiG1qXWgShAq7nQCgH70ok0U8tfrrx0RmJP8XvxuRFZk8g8K2Xj-cYK1fZ6UbkHtBb4h4VFqjjTXw4JwmT8AJ9_TRdqJ84Pfb1Is39S_BLcSLwAxdZ5c9r4gpCOxTG_-WPG9UcH8W17EZHcnhifhPXlzsNGd2WhhPJDE8QWZZ8k9rc_0Xw4dgkLHLKgHcvD0sFSyu6ifvWEjx3VMaVvDNKbJ5-ZmJk-reK4_x0_Zj8sQfnvX2Q8KrDEYIo8qpu81dV71t4-gfZ54qaK5wexWOQQGhHbvNhnCbjrWPfqaQjGLpp38j1EzrX5paHjXpofzWtavEovK_jxgWUX_fOVDsPlejxtFXHRqwbGysR3_hWcV=w939-h612-no "Login")

* Login success

![Login Success](https://lh3.googleusercontent.com/XE7aNLSkcQ9gbpv5B6kIEaMgknoj28NmW8J4jOmYLDVfz1U5PheTU8_X_8K30sepbuQrcprHJWjsUVktB9vpbjH-FAm9tCYVrck4s-s27dNOa-_l_RLJOY04Z_wrFEP-uMfdKBaovQLEszi_SzxOvrYDBtZe_4hEvJ4q_QQAuUIVtSWoCqg0joJBnr_jV59z7fNna2Oe453WJLrSwKQAnCA0EYc39JQx_NJ5sjWdNruzytk9woeFJa1-sLJxxg1dDztvYT1YNUv7uyNAXIClUkwkMRPG1jYGJBod3tt5dOna4xEq5yIhayjoml7gwfHIm56hSYPmLETEvaQRgUTmdpC0lpVLDPLJtnr7ULelFiJsiIutVqzasCDi6U0fYxW62Z_rMbgkBRkadMJVj2KzIAOo9Jgopv7515ZrOTsIR0xtupRv1G2JnrhkrUM52Lktf7SiS9KuwkVRpn1gESpr9voK70y8xbQpZl-BrYsebc9Mb95GiPddB6ajPd3oCceUjdDqzDDJLKgcFtyW5rFWCPogyjCpKhiitI5w8ntZqSnNyMXcGXW2AFaygpNt3AwF9uV-7PTCeW0dX0b9HDRUwhA8EYVq8i9vx3dkMFKeR3c5OLuoSaxCyLgyOkXHJ2m6BzbcM6P3owPcApwnjIynw9sq8XYwL93CPWSPU-XGei5RGyV-uuHwM2U0TdfFE0CiTawMrHuus14yG9lY51V1eb08R_F8vnBh_Ep9rQnjp2eyhOwH=w928-h599-no "Login Success")


![WS Call](https://lh3.googleusercontent.com/unyKUaOsC0Yuhv-tUanf-Y9BgE1dwGOet9giLyUMfuRnkULMDRNiD5_-Y-ejgn1XIP-VNItiHuTr3ON5Ux9ZhExEA1KWEWCSoF0WBi67PDJEfz54WUO3dHrfnfAfcxhQQwn_UFYJLIXipDVH88OiHl7jtojgHayYzT-8JcqYWuY29R9BoNXm2rrc_sKQp2tF9JuRDoE2z4bbu4ZNk8KFRq9I75CVDEz9j5u_8zyHGFSeySn4QC3CArlGkc3Dr4asd9yhad1kWS7vgG-rWbtocOJYnjfEgDqrAgTlH-oSyJ7YQEy_aE9i7bFYPmZuL9zWMRq5YiMsLGmciC1HDURwnPeUuiJOSrMiy2hQlRvPShT8zC5doU33vq_Kzhi95Flrd1DaISoc0nv3lMpMXHl92hOnUCkYDEN54nmglRocOz6PPHrRjB7lWuHNLD7d1p2CzRkGoNQn91ErF8suDp1QTXCHms5hBjq6WRti3txpUS6EQGpbz2V5EE1eRgoppvRaysfhmB_iKcne81axQcj3MMAXdCf_Ad1KWczN8SKDR3JOsihJ5Bud21dfOdl5ixkv6qmnJM35vKguoB-IT1KwHqoucdutILUt9stU8YZ_ctDObe0uWN5Qh1Kfn6Qe-sKuB68IQJkFU60HyVibXzGzRXqKg2TZGLhpGL2QeP0ZzCeV01p2oYmRxZhkgmBnnzwa8IaWvaHY2d7LOr_70wqGKIIYbnnoQjdSRCdAvyeGf6wfViSw=w1030-h633-no "WS Call")

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
sudo certbot --apache -d oriontec.de -d www.oriontec.de
keytool -import -alias tomcat -file /etc/letsencrypt/live/oriontec.de/cert.pem -keystore keystore.p12 -storepass password
keytool -importkeystore -srckeystore keystore.p12 -destkeystore keystore.p12 -deststoretype pkcs12
openssl pkcs12 -export -in fullchain.pem -inkey privkey.pem -out /opt/postmail/classes/keystore.p12 -name tomcat -CAfile chain.pem -caname root
```








