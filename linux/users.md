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

## who

```shell
who
```

## groups

Get groups from a specific user:
```shell
groups signet
```

## useradd

Print useradd configuration:
```shell
useradd -D
```

Create a user:
```shell
adduser signet --comment "" --disabled-password
```

```shell
useradd signet -m
```

Delete a user:
```shell
sudo userdel -r signet
```

Add user to group:
```shell
usermod -aG <group> signet
```

Verify sudo access:
```shell
sudo -l -U signet
```

## Related links

- https://linuxhandbook.com/check-if-user-has-sudo-rights/
- https://linuxhandbook.com/create-sudo-user/
- https://linuxhandbook.com/userdel-command/
- https://www.golinuxcloud.com/add-user-to-sudoers/
- https://linuxopsys.substack.com/p/creating-and-managing-user-accounts
