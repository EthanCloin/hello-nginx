# Goal
Learn how to use Nginx as a web server to render some static content.

Ultimately I want to have hypermedia servers hosted on some cloud service or CDN with whatever
sites / apps I develop

Nginx is often recommended for use as a reverse proxy. Maybe I use it to have one VPS accept
requests and route it to the appropriate application that is running as a docker container
on that machine. 

I also don't have much understanding of docker so building an nginx image will help there.

# Quickstart
You need Docker Desktop on your machine. That should be the only dependency.

## Option One: Build with Docker Compose
```bash
docker compose up
```

## Option Two: Build with Docker
1. Build the Docker image
```bash
docker build -t hello-nginx
```

1. Run the Docker image as a container instance
```bash
docker run -it --rm -p 8080:80 hello-nginx
```

Visit localhost:8080 to see the rendered html file
