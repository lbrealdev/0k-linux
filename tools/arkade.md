# Arkade - Open Source Marktplace Tools

**Arkade** is an amazing tool, see more about it here:

- [arkade - Open Source Marketplace For Developer Tools](https://github.com/alexellis/arkade)

## Install arkade

Install arkade for linux:
```shell
curl -sLS https://get.arkade.dev | sudo sh
```

## Update arkade

Delete binary in /usr/local/bin:
```shell
rm -rf /usr/local/bin/arkade
```

Remove cached versions of tools:
```shell
rm -rf $HOME/.arkade
```

Install arkade again, run:
```shell
curl -SLfs https://get.arkade.dev | sudo sh
```

## Install go with arkade:

1 - Install arkade:
```shell
curl -sLS https://get.arkade.dev | sudo sh

arkade --help
```

2 - Install go with arkade:
```shell
arkade system install go
```

3 - Export environments variables to use go:
```shell
export PATH=$PATH:/usr/local/go/bin:$HOME/go/bin
export GOPATH=$HOME/go/

source .bashrc
```

4 - Verify go version:
```shell
go version
```

## Upgrade go version with arkade:

1 - Delete go binary:
```shell
sudo rm -rf /usr/local/go
```

2 - Install go with arkade:
```shell
arkade system install go
```

3 - Verify go version:
```shell
go version
```
