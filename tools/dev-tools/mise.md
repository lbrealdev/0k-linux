# mise

mise - dev tools, env vars, task runner

## Sources

- Website: https://mise.jdx.dev/
- GitHub Repository: https://github.com/jdx/mise/

## Usage

### Install

Download `mise` binary from GitHub release page:
```shell
curl -fsSLo "mise" "https://github.com/jdx/mise/releases/download/v2025.8.18/mise-v2025.8.18-linux-x64"
```

Move `mise` binary to `/usr/local/bin`:
```shell
sudo mv mise /usr/local/bin/
```

Change `mise` binary permissions:
```shell
sudo chmod +x /usr/local/bin/mise
```

Update `~/.bashrc` with `mise` settings:
```shell
echo 'eval "$(mise activate bash)"' >> ~/.bashrc

echo 'export PATH=$HOME/.local/share/mise/shims:$PATH' >> ~/.bashrc
```

### Uninstall

// to do

### Update

Update `mise` version:
```shell
mise self-update
```

### Settings

```shell
mise settings set experimental true
```

### Manage Tools

List installed and active tools:
```shell
mise ls
```

Gets information about a tool:
```shell
mise tool python
```

Install `node`:
```shell
mise use --global node@22
```

Install `mermaid-cli`:
```shell
mise use -g npm:@mermaid-js/mermaid-cli

mise uninstall npm:@mermaid-js/mermaid-cli
```

Install `aws-cli`:
```shell
mise use aws-cli
```
