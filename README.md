# Using keycloak with Spring-boot
## Keycloak
#### Start keycloak
```
docker run --rm -e KEYCLOAK_USER=admin -e KEYCLOAK_PASSWORD=pwd -p 8180:8080 jboss/keycloak:4.8.3.Final
```
#### Configure keycloak
* Browse the keycloak admin console http://localhost:8180/auth/admin/master/console/#/realms/login-realm:
* Import realm configuration from file src/main/resources/realm-export.json.

# Behaviour
## get token
```
curl -X POST -i\
    -H "Content-Type: application/x-www-form-urlencoded" \
    -d 'username=user1&password=password&grant_type=password' \
    -d 'client_id=login-app' \
    -d 'client_secret=dummy' \
    "http://localhost:8180/auth/realms/login-realm/protocol/openid-connect/token"
```
