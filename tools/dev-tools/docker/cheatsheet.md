# Docker Cheat Sheet

Delete all containers:
```shell
docker rm -f $(docker ps -a --format {{.ID}})
```

Check docker disk usage:
```shell
docker system df
```

Remove docker unused data:
```shell
docker system prune -a --volumes -f
```
