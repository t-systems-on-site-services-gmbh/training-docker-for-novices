# Docker

```
docker build -t getting-started PATH
````
Build a container image from a Dockerfile.

- `PATH` the path to the Dockerfile
- `-t getting-started` name the image


```
docker run -d -p 80:80 getting-started
```
Run a container.

- `-d` detached mode (run in background) 
- `-p 80:80` map port 80 of host to port 80 in the container 
- `docker/getting-started` the image to use 
- `-v todo-db:/etc/todos` map docker volume `todo-db` to path `/etc/todos` in the container
- `-w /app` use container's directory `/app` as working dir
- `--network todo-net` attach the container to network `todo-net`, used for multi-container apps
- `--network-alias app` use `app` as container's name in the network


```
docker container ls
```
List running containers, also `docker ps`.


```
docker image ls
```
List container images.


```
docker stop <container-id>
```
Stop the container `<contained-id>`.


```
docker rm <container-id>
```
Remove the container `<contained-id>`.
Use `-f` to stop the container before removing it.


```
docker exec <container-id> <command>
```
Execute the `<command>` in container `<contained-id>`.

- `-i` interactive mode
- `-t` allocate a pseudo-TTY


```
docker volume create todo-db
```
Create a volume named `todo-db`.


```
docker volume inspect todo-db
```
Inspect the volume `todo-db`, e.g. see the location on the file system.


```
docker logs -f <container-id>
```
Watch the logs of container `<container-id>`.


```
docker network create todo-net
```
Create the network `todo-net`
