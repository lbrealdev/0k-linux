# Docker

### Docker Engine on Debian

- [Install using the apt repository](https://docs.docker.com/engine/install/debian/#install-using-the-repository)
- [Install from a package](https://docs.docker.com/engine/install/debian/#install-from-a-package)
- [Uninstall Docker Engine](https://docs.docker.com/engine/install/debian/#uninstall-docker-engine)

### Docker Desktop on Debian

- [Install Docker Desktop](https://docs.docker.com/desktop/install/linux/debian/#install-docker-desktop)
- [Uninstall Docker Desktop](https://docs.docker.com/desktop/uninstall/)

Install docker engine via `apt`:
```shell
apt-cache madison docker | awk '{ print $3 }'

apt-cache policy docker*
```

```shell
# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/debian/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/debian \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update


sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

sudo usermod -aG docker $USER
```

MX Linux SysVinit
```shell
sudo service docker status
```

Install using the convenience script:
```shell
curl -fsSL https://get.docker.com  | sudo sh
```

#### Source

- https://github.com/docker/docker-install

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

Build an image from a __`Dockerfile`__:

Build with tag latest
```shell
docker build -t swagger .
```

Build with the repository name and the latest tag
```shell
docker build -t datteops/swagger .
```

Build with the name of the repository and with the v1.0 tag
```shell
docker build -t datteops/swagger:v1.0 .
```

### docker image

- [source](https://docs.docker.com/reference/cli/docker/image/)

List images:
```shell
docker images
```

### docker run

Run a command in a new container:
```shell
docker run -d -p 8080:8080 --name service-swagger datteops/swagger:v1.0
```

### docker ps

_List containers_

List only containers running:
```shell
docker ps
```

List all containers running and stopped:
```shell
docker ps -a
```

### docker stop

Stop one or more running containers

Stop with container name
```shell
docker stop service-swagger
```

Stop with container ID:
```shell
docker stop 52c2d69953a9
```

### docker start

Start one or more stopped containers.

Start with container nome:
```shell
docker start service-swagger
```

Start with container ID:
```shell
docker start 52c2d69953a9
```

### docker logs

Fetch the logs of a container

Get logs with container name:
```shell
docker logs service-swagger
```

Get logs with container ID:
```shell
docker logs 52c2d69953a9
```

### docker rm

Remove one or more containers

Remove container by name:
```shell
docker rm service-swagger
```

Remove container by ID:
```shell
docker rm 662c38240042
```

### docker stats

Display a live stream of containers resource usage statistics:
```shell
docker stats
```

### Repositories

- https://github.com/GoogleContainerTools/distroless
- https://github.com/hotheadhacker/awesome-selfhost-docker

### Registries

- https://images.chainguard.dev/

### Docker Guides, Blogs and Tutorials

- [Dockerdocs - Building best practices](https://docs.docker.com/build/building/best-practices/)
- [How to Build Smaller Container Images: Docker Multi-Stage Builds](https://labs.iximiuz.com/tutorials/docker-multi-stage-builds)
