# ssh

ssh — OpenSSH SSH client (remote login program)

## Contents

- [Installation](#installation)
  - [Verify client](#verify-client)
  - [Verify server is running](#verify-server-is-running)
  - [Verify firewall allows SSH](#verify-firewall-allows-ssh)
- [Usage](#usage)
  - [ssh-agent](#ssh-agent)
  - [Config files](#config-files)
  - [Generate an SSH key](#generate-an-ssh-key)
  - [Identity file](#identity-file)
- [Related links](#related-links)

## Installation

Search OpenSSH packages:
```shell
apt search openssh | grep -E 'openssh-client|openssh-server'
```

Install the client (`ssh`, `scp`, `ssh-keygen`, `ssh-copy-id`):
```shell
sudo apt install openssh-client
```

Install the server only if this machine should accept SSH logins:
```shell
sudo apt install openssh-server
```

Install netstat:
```shell
sudo apt install net-tools
```

### Verify client

The SSH client is not a daemon:
```shell
ssh -V
```

### Verify server is running

Debian/Ubuntu:
```shell
systemctl status ssh
```

RHEL/Fedora:
```shell
systemctl status sshd
```

Start and enable on boot if needed (Debian/Ubuntu):
```shell
sudo systemctl enable --now ssh
```

SysVinit (MX Linux, Debian without systemd):
```shell
sudo service ssh status
```

```shell
sudo /etc/init.d/ssh status
```

Start and enable on boot if needed:
```shell
sudo service ssh start
sudo update-rc.d ssh defaults
```

Confirm it is listening (default port 22):
```shell
ss -tlnp 'sport = :22'
```

```shell
sudo netstat -tlnp | grep ssh
```

### Verify firewall allows SSH

ufw (Ubuntu, Debian, MX if installed):
```shell
sudo ufw status
```

Allow SSH if the firewall is active and 22 is not listed:
```shell
sudo ufw allow OpenSSH
```

firewalld (RHEL/Fedora):
```shell
sudo firewall-cmd --state
sudo firewall-cmd --list-services
```

Allow SSH if needed:
```shell
sudo firewall-cmd --permanent --add-service=ssh
sudo firewall-cmd --reload
```

If neither ufw nor firewalld is in use:
```shell
sudo iptables -L INPUT -n | grep -E '22|ssh'
```

```shell
sudo nft list ruleset
```

## Usage

### ssh-agent

```shell
eval `ssh-agent -s`
```

### Config files

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

### Identity file

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
