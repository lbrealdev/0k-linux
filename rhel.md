# Red Hat Enterprise Linux

Show status information for this system's subscriptions and products:
```
subscription-manager status
```

Print version information
```
subscription-manager version
```

List subscription and product information for this system:
```
subscription-manager list
```

#### Repos
List the repositories which this system is entitled to use

List all known repositories for this system:
```
subscription-manager repos --list
```
List known, enabled repositories for this system:
```
subscription-manager repos --list-enabled
```
List known, disabled repositories for this system:
```
subscription-manager repos --list-disabled
```

#### YUM
```
yum repolist
```
#### RHSM configuration
```
cat /etc/rhsm/rhsm.conf
```
