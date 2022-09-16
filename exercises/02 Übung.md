# Übung

Erstelle dein erstes Container Image.

Auf der VM liegt im Verzeichnis `todoapp` eine kleine Node-Anwendung. Erstelle ein `Dockerfile` für die Anwendung.

```
FROM node:12-alpine
WORKDIR /app
COPY package.json yarn.lock ./
RUN yarn install --production
COPY . .
CMD ["node", "src/index.js"]
```

Erstelle nun das Image mit dem Befehl `docker build` und nenne es *todoapp*.

Starte anschließend den Container mit

```
docker run -dp 3000:3000 todoapp
```

Öffne einen Browser und lade die todoapp. Erzeuge einige Todo-Items.

Starte den Container neu und aktualisiere die todoapp im Browser. Was ist passiert?
