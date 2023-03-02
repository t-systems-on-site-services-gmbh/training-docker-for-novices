# Übung

Erstelle eine docker-compose.yml, um die beiden Container aus der vorherigen Übung (todoapp und mysql) zu starten.

Zur Hilfestellung hier ein Fragment:
```
version: "3.7"

services:
    todoapp:
        image: node:12-alpine
        command: sh -c "yarn install && yarn run dev"
        ports:
            - 3000:3000
        working_dir: /app
        volumes:
            - ./:/app
        environment:
            - MYSQL_HOST=mysql
            ...
    mysql:
        image: mysql:5.7
        volumes:
            ...
```
