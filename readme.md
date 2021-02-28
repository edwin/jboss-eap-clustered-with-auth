Create a Protected JBoss EAP UDP Cluster with Authentication
===================

Purpose
-------------------
Create a simulation of a protected JBoss EAP cluster by using a multiple containerized Keycloak instances.  

Tools
-------------------
* Docker
* Keycloak container image

How To
-------------------
Build image
```
docker build -t mykeycloak .
```

Run image
```
docker run -p 8081:8080 -e PROXY_ADDRESS_FORWARDING=true  -e DB_VENDOR="mysql" -e DB_ADDR="192.168.56.1" -e DB_USER="keycloak" -e DB_PASSWORD="password" -e DB_PORT="3306" -e DB_DATABASE="keycloak_db" --add-host=HOST:192.168.56.1  mykeycloak
```

Blog
--------------------
```
https://edwin.baculsoft.com/2021/02/create-a-protected-jboss-eap-udp-cluster-with-authentication/
```
