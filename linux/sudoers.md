# sudoers

Edit `sudoers` file:
```shell
sudo visudo
```

Allow user to use `sudo` without passoword:
```shell
your_username ALL=(ALL) NOPASSWD:ALL
```

Allow all users in a specific group to use `sudo`:
```shell
%your_group ALL=(ALL) NOPASSWD:ALL
```

Sudo configuration file:
```shell
/etc/sudoers
```
