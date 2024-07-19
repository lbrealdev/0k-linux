 # systemd

systemd, init - systemd system and service manager

## Usage

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

### Source

- [Systemd's web site](https://systemd.io/)
- [Systemd repository](https://github.com/systemd/systemd)

### Systemd articles

- [Announcing systemd v256](https://0pointer.net/blog/announcing-systemd-v256.html)
- [systemd for Administrators - part 1](https://0pointer.net/blog/projects/systemd-for-admins-1.html)
- [systemd for Administrators - part 2](https://0pointer.net/blog/projects/systemd-for-admins-2.html)
- [systemd for Administrators - part 3](https://0pointer.net/blog/projects/systemd-for-admins-3.html)
- [systemd for Administrators - part 4](https://0pointer.de/blog/projects/systemd-for-admins-4.html)

### Systemd Blogs

- [Unlocking LUKS2 volumes with TPM2, FIDO2, PKCS#11 Security Hardware on systemd 248](https://0pointer.net/blog/unlocking-luks2-volumes-with-tpm2-fido2-pkcs11-security-hardware-on-systemd-248.html)

**If you wonder why many people don't like systemd, maybe this link will help you.**

- https://nosystemd.org/
