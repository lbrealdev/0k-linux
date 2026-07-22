# ssh

ssh — OpenSSH SSH client (remote login program)

## Usage

```shell
eval `ssh-agent -s`
```

Search **openssh** package using `apt`:
```shell
apt search openssh | grep -E 'openssh-client|openssh-server'
```

```shell
netstat -tunapl | grep 22
```

SSH config file:
```shell
/etc/ssh/ssh_config
```

Check the configuration file:
```shell
sudo sshd -t
```

### Generate an SSH key

Run this on the client:
```shell
ssh-keygen -t rsa -b 4096 -C "bitcoinprovocamaremoto@togeda.io"
```

Copy the public key to the server:
```shell
ssh-copy-id -i ~/.ssh/id_rsa.pub user@server
```

When the public key is on the remote server, connect as follows:
```shell
ssh user@server
```

Convert to PEM format:
```shell
cp ~/.ssh/id_rsa ~/keys/id_rsa.pem
```

```shell
ssh -i ~/keys/id_rsa.pem user@server
```

## Related links

- [Visual guide to SSH tunneling and port forwarding](https://ittavern.com/visual-guide-to-ssh-tunneling-and-port-forwarding/)
- [ssh-audit Primer - Audit your SSH Server](https://ittavern.com/ssh-audit-primer-audit-your-ssh-server/)
- [SSH Troubleshooting Guide](https://ittavern.com/ssh-troubleshooting-guide/)
- [SSH Server Hardening Guide v2](https://ittavern.com/ssh-server-hardening/)
- [An Excruciatingly Detailed Guide To SSH (But Only The Things I Actually Find Useful)](https://grahamhelton.com/blog/ssh-cheatsheet/)
- [How SSH Secures Your Connection](https://noratrieb.dev/blog/posts/ssh-security/)
