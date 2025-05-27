# sed

sed - stream editor for filtering and transforming text

## Usage

Replace `1Gi` with `10Gi` only lines that contain __storage__:
```shell
sed -i '/storage/ s/1Gi/10Gi/g' az-pvc.yml
```

Add text in line 5:
```shell
sed -i '5i\  namespace: sigma' az-pvc.yml
```

Delete line 5:
```shell
sed -i '5d' az-pvc.yml
```

Comment line 3 with # and add `nameserver ip` to the last line in resolv.conf file:
```shell
sed -i -e '3s/^/# /' -e '$ a nameserver 180.100.250.01' /etc/resolv.conf
```

# Related links

- [Everything you need to know about sed substitution](https://learnbyexample.github.io/everything-about-sed-substitution/)
