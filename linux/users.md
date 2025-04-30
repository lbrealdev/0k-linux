# Linux - Managing users

## Usage

### List Linux users

```shell
cat /etc/passwd
```

```shell
getent passwd
```

```shell
compgen -u
```

### List all the connected users

```shell
who
```

### Print the groups for a user

```shell
groups signet
```

### Create a user

```shell
adduser signet --comment "" --disabled-password
```

```shell
useradd signet -m
```

### Delete a user

```shell
sudo userdel -r signet
```

### Add user to group

```shell
usermod -aG <group> signet
```

### Verify sudo access

```shell
sudo -l -U signet
```

## Related links

- https://linuxhandbook.com/check-if-user-has-sudo-rights/
- https://linuxhandbook.com/create-sudo-user/
- https://linuxhandbook.com/userdel-command/
