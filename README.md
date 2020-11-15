# Docker-Note

## Image
Build a new images.
```
docker pull ubuntu
```

## Container

### Create a instance of image.
```
docker run --name WHATEVER_YOU_LIKE -d -p 8080:80 ubuntu
```

Create a container with volumes.
```
docker run --name WHATEVER_YOU_LIKE -v $(pwd):PATH_IN_CONTAINER -d -p 8080:80 ubuntu
```

Run a existed container.
```
docker start CONTAINER_NAME
```

Stop a running container.
```
docker stop CONTAINER_NAME
```

(Optional) Read only.
```
docker run --name CONTAINER_NAME -v $(pwd):PATH_IN_CONTAINER:ro -d -p 8080:80 ubuntu
```

Interactive mode.
```
docker run --name CONTAINER_NAME -dit ubuntu
docker exec -it CONTAINER_NAME bash
```

### Remove a instance of image.
```
docker rm CONTAINER_ID
```

### Remove containers
```
docker rm -f CONTAINER_NAME
```
```
docker container prune
```

### View all containers
```
docker ps --format=$FORMAT
```
