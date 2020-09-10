php index.php

HOST="172.17.0.1"
KEYCLOAK_URL="http://${HOST}:8080/auth"
SERVICE_URL="http://${HOST}:8082"
docker run -it --rm -p 8083:80 -v $PWD:/var/www/html -e KEYCLOAK_URL=${KEYCLOAK_URL} -e SERVICE_URL=${SERVICE_URL} php:7.2-apache

