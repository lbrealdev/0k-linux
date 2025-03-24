# Docker Cheat Sheet

Delete all containers:
```shell
docker rm -f $(docker ps -a --format {{.ID}})
```
