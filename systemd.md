 # systemd

List all services:
```shell
systemctl list-units --type service --all
```

List all timers:
```shell
 systemctl list-units --type timer --all
```

List all targets:
```shell
 systemctl list-units --type target --all
```
 
List unit file and show state:
```shell
 systemctl list-unit-files --full
```

List unit file for timers:
```shell
 systemctl list-unit-files --type timer
```

List unit file for targets:
```shell
 systemctl list-unit-files --type target
```

List unit file for services:
```shell
 systemctl list-unit-files --type service
```

Show service unit file:
```shell
 systemctl cat sshd.service
```
