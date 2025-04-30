# Docker

### Docker command guide

<!-- TOC -->

- [docker info](#docker-info)
- [docker login](#docker-login)
- [docker build](#docker-build)
- [docker images](#docker-images)
- [docker run](#docker-run)
- [docker ps](#docker-ps)
- [docker start](#docker-start)
- [docker stop](#docker-stop)
- [docker stats](#docker-stats)
- [docker system](#docker-system)

### docker info

Display system-wide information:
```shell
docker info
```

### docker login

Log in to a Docker registry:
```shell
docker login
```

### docker build

Build an image from a `Dockerfile`.

Build with tag latest:
```shell
docker build -t swagger .
```

Build with the repository name and the latest tag:
```shell
docker build -t datteops/swagger .
```

Build with the name of the repository and with the v1.0 tag:
```shell
docker build -t datteops/swagger:v1.0 .
```

### docker images

List images:
```shell
docker images
```

### docker run

Run a new container:
```shell
docker run -d -p 8080:8080 --name service-swagger datteops/swagger:v1.0
```

### docker ps

List only containers running:
```shell
docker ps
```

List all containers running and stopped:
```shell
docker ps -a
```

### docker stop

Stop with container name:
```shell
docker stop service-swagger
```

Stop with container ID:
```shell
docker stop 52c2d69953a9
```

### docker start

Start with container name:
```shell
docker start service-swagger
```

Start with container ID:
```shell
docker start 52c2d69953a9
```

### docker logs

Get logs with container name:
```shell
docker logs service-swagger
```

Get logs with container ID:
```shell
docker logs 52c2d69953a9
```

### docker rm

Remove container by name:
```shell
docker rm service-swagger
```

Remove container by ID:
```shell
docker rm 662c38240042
```

### docker rmi

Remove image by ID:
```shell
docker rmi 44f22c911346
```

### docker stats

Display a live stream of containers resource usage statistics:
```shell
docker stats
```

### docker system

Check docker disk usage:
```shell
docker system df
```

Remove docker unused data:
```shell
docker system prune -a --volumes -f
```

### Repositories

- https://github.com/GoogleContainerTools/distroless
- https://github.com/hotheadhacker/awesome-selfhost-docker

### Registries

- https://images.chainguard.dev/
