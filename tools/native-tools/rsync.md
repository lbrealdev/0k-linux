# rsync

rsync - a fast, versatile, remote (and local) file-copying tool

### Sources

- https://rsync.samba.org/
- https://github.com/RsyncProject/rsync
- https://terminaltrove.com/rsync/

### Usage

Copy file from local to remote host:
```shell
rsync -avzP <file-to-copy> <hostname>@<ip-address>:<destination-directory>
```

Copy file from remote host to local:
```shell
rsync -avzP <hostname>@<ip-address>:<file-to-copy> <destination-directory>
```
