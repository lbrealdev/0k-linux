# find
```
find /var/local/* -maxdepth 1 -type d -mtime 7 -print
```

```
find ./ -print 2>&1 | grep "$item"

find ./ -print 2>&1 | grep -Rin "$item"
```

```
find /home/user/ -name main.yml -ls
```
