# docker-hello-world
Docker "Hello World"

To execute: `docker build -t public .`

To list images: `docker images`

To run docker: `docker run -it -p 80:80 public`

The -it flag will make sure the output of the container is forwarded to the terminal.

The -p flag instructs Docker that we want the internal port to 80 to be available on port 80 on the host machine. All traffic to port 80 will be forward to port 80 in the container.