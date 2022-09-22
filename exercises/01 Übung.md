# Übung 

Erste Gehversuche. Bekomme ein Gefühl für Docker und experimentiere ein bisschen an der Kommandozeile.

```
docker run hello-world
```

Führt den Container `hello-world` aus. Lies dir die Ausgabe aufmerksam durch und probiere den Befehl

```
docker run -it ubuntu bash
```
aus.

Lass dir mittels

```
docker image ls
```

die verfügbaren Images anzeigen. Analog dazu listet

```
docker container ls --all
```
alle Container auf.

Versuche das Image `hello-world` mit folgendem Befehl zu entfernen.

```
docker image rm hello-world
```

Was muss vorher gemacht werden? Wie kannst du anschließend deinen Erfolg kontrollieren?
