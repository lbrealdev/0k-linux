# dpkg

dpkg - package manager for Debian

## Usage

Configure a package which has been unpacked but not yet configured:
```shell
sudo dpkg --configure -a
```

```shell
dpkg -l
```

```shell
dpkg-query -W
```

```shell
dpkg-query -W <package>
```

```shell
dpkg-query -W --showformat='${Package} ${Version}\n'
```

```shell
sudo dpkg -P <package>
```
