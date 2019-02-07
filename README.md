# Using keycloak with Spring-boot
## Keycloak
#### Start keycloak
```
docker run --rm -e KEYCLOAK_USER=admin -e KEYCLOAK_PASSWORD=pwd -p 8180:8080 jboss/keycloak:4.8.3.Final
```
#### Configure keycloak
* Browse the keycloak admin console http://localhost:8180/auth/admin/master/console/#/realms/login-realm:
* Import realm configuration from file src/main/resources/realm-export.json.