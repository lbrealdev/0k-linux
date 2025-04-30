# Docker

### Install Docker Engine using APT

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
```

```shell
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

#### Sources

- https://github.com/docker/docker-install
- [Install using the apt repository](https://docs.docker.com/engine/install/debian/#install-using-the-repository)
- [Install from a package](https://docs.docker.com/engine/install/debian/#install-from-a-package)
- [Uninstall Docker Engine](https://docs.docker.com/engine/install/debian/#uninstall-docker-engine)
- [Install Docker Desktop](https://docs.docker.com/desktop/install/linux/debian/#install-docker-desktop)
- [Uninstall Docker Desktop](https://docs.docker.com/desktop/uninstall/)

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
