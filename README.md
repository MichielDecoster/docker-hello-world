# docker-hello-world
Docker "Hello World"

## To execute: 
```
docker build -t public .
```

## To list images: 
```
docker images
```

## To run docker: 
```
docker run -it -p 80:80 public
```

### The -it flag
Will make sure the output of the container is forwarded to the terminal.

### The -p flag 
Instructs Docker that we want the internal port to 80 to be available on port 80 on the host machine. All traffic to port 80 will be forward to port 80 in the container.

Reference: https://docs.docker.com/engine/reference/run/

## Determine Docker IP address : 
```
docker-machine ip
```

### The -d flag:
Makes it possible to run containers in the background. Easily combined with the `docker run` command.
```
docker run -d -p 80:80 public
```

## Running Containers
```
docker ps
```
Shows the running containers

## Stopping Containers
```
docker stop <container_id/name>
```
