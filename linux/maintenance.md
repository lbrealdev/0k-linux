# Maintenance

Delete user trash:
```shell
rm -rf .local/share/Trash/*
```

Clear cached memory, freeing up RAM:
```shell
sudo su

free -wht && sync && echo 3 > /proc/sys/vm/drop_caches && free -wht
```
