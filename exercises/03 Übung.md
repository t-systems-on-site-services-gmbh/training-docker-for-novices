# Übung

Erstelle ein Netzwerk `todoappnet` und starte einen Container mit MySQL in diesem Netzwerk.

```
docker network create todoappnet
docker run -d --network todoappnet --network-alias mysql \
    -v todo-data:/var/lib/mysql \
    -e MYSQL_ROOT_PASSWORD=secret \
    -e MYSQL_DATABASE=todos \
    mysql:5.7
 ```
 
 **Warnung** Übergib Passwörter niemals in Umgebungsvariablen!
 
 Starte den Container der Todo-App im Netzwerk `todoappnet`. Übergib dabei die Umgebungsvariablen `MYSQL_HOST`, `MYSQL_USER`, `MYSQL_PASSWORD` und `MYSQL_DB`. 
 Lass dir die Log-Ausgaben des Containers anzeigen.
 
 ```
 docker logs -f <container_id>
 ```
 
 Erstelle einige Todo-Items, stoppe und starte den Container. Sind die Items immer noch da?
 
 
 ## Bonusaufgabe
 
 * Führe im MySQL-Container das Kommando `mysql` aus und lass dir die Datenbanken mit dem Befehl `SHOW DATABASES;` anzeigen.
 * Modifiziere ein oder zwei Todo-Items in der Tabelle `todo_items` und aktualisiere die Anwendung im Browser.
 
