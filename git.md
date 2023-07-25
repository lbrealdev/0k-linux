# git

### Use

Check Git version:
```shell
git --version
```

Check installed Git version using package manager:
```shell
apt list --installed | grep git

apt-cache policy git
```

Get more information about available Git versions from your packager manager:
```shell
apt-cache madison git
```


```shell
cat /var/lib/apt/lists/

cat /var/lib/apt/lists/deb.debian.org_debian_dists_bullseye_main_binary-amd64_Packages | grep "Package: git"
```

```shell
apt-cache search ^git

apt-cache show git

apt list --installed | grep "git/oldstable"

dpkg --get-selections | grep git

dpkg -l

apt-mark showmanual

apt list --manual-installed


sudo apt install build-essential

apt list --installed | grep build


sudo apt-get remove git

sudo apt-get purge git

sudo apt-get remove --auto-remove git

sudo apt-get purge --auto-remove git



Install from source

sudo apt-get install dh-autoreconf libcurl4-gnutls-dev libexpat1-dev gettext libz-dev libssl-dev

sudo apt-get install asciidoc xmlto docbook2x

sudo apt-get install install-info

curl -SLfs https://mirrors.edge.kernel.org/pub/software/scm/git/git-2.39.2.tar.gz -o git.tar.gz

curl -SLfs https://github.com/git/git/archive/refs/tags/v2.39.3.tar.gz -o git-2.39.3.tar.gz

 
tar -zxf git-2.39.3.tar.gz


curl -SLfs https://github.com/git/git/archive/refs/tags/v2.39.3.tar.gz -o git-2.39.3.tar.gz

tar -xvf git-2.39.3.tar.gz

cd git-2.39.3/

make configure

./configure --prefix=/usr

make all doc info

sudo make install install-doc install-html install-info
```

