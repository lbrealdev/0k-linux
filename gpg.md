# GPG - GnuPG

Get gpg version:
```shell
gpg --version
```

### Manage your keyring

List all keys in public keyring:
```shell
gpg --list-keys --keyid-format=long
```

List all keys with signature:
```shell
gpg --list-sigs --keyid-format=long
```

Delete keys from public keyring:
```shell
gpg --delete-keys <key-id>
```

Delete keys from private keyring:
```shell
gpg --delete-secret-keys <key-id>
```

List keys in private keyring:
```shell
gpg --list-secret-keys --keyid-format=long
```

```shell
gpg --status-fd=2 -bsau <gpg-key-id>
```

Get fingerprint from public key:
```shell
gpg --fingerprint <user-id>
```

