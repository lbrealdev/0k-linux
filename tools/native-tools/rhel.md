# Red Hat Enterprise Linux

Show status information for this system's subscriptions and products:
```shell
subscription-manager status
```

Print version information
```shell
subscription-manager version
```

List subscription and product information for this system:
```shell
subscription-manager list
```

#### Repos
List the repositories which this system is entitled to use

List all known repositories for this system:
```shell
subscription-manager repos --list
```
List known, enabled repositories for this system:
```shell
subscription-manager repos --list-enabled
```
List known, disabled repositories for this system:
```shell
subscription-manager repos --list-disabled
```
Repository to enable:
```shell
subscription-manager repos --enable=REPOID
```
Repository to disable:
```shell
subscription-manager repos --disable=REPOID
```

#### YUM
```shell
yum repolist
```
#### RHSM configuration
```shell
cat /etc/rhsm/rhsm.conf
```
