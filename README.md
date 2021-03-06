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

## To run docker image with name

```
docker run --name <image>
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
Makes it possible to run containers in the background (detached mode). Easily combined with the `docker run` command.
```
docker run -d -p 80:80 public
```

## Running Containers
```
docker ps
```
Shows the running containers

```
docker ps -a
```
Shows running aswell as previously stopped containers

## Stopping Containers
```
docker stop <container_id/name>
```

## Remove Containers
```
docker rm <container_id/name>
```

## Docker Images
```
docker images
```
Lists images & sizes.

To remove images:
```
docker rmi <image_name>
```
Make sure no containers are running of that image

## Pulling images without running
```
docker pull <image_name>
```

## Containers are not meant to host Operating Systems

They are meant to run images. It only lives as long as the process is alive.

## Sleep command

Used to let a container sleep for x amount of time (in this example 5 seconds)
```
docker run ubuntu sleep 5
```

## Docker exec command
```
docker exec <container_id/name> cat /etc/hosts
```
Runs a command on the docker container

## Running older version of a image
```
docker run <image>:<version>
```
If not specified automatically runs :latest