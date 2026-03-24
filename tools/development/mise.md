# mise

mise - dev tools, env vars, task runner

## Sources

- https://mise.jdx.dev/
- https://github.com/jdx/mise/
- https://mise-versions.jdx.dev/

## Usage

### Install

Download `mise` binary from GitHub release page:
```shell
curl -fsSLo "mise" "https://github.com/jdx/mise/releases/download/v2025.11.8/mise-v2025.11.8-linux-x64"
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
```

Add shims path to the PATH environment variable:
```shell
echo 'export PATH=$HOME/.local/share/mise/shims:$PATH' >> ~/.bashrc
```

### Option

```shell
curl -s https://mise.run | sh
```

```shell
echo 'eval "$(mise activate bash)"' >> ~/.bashrc
```

### Shim

```shell
mise reshim
```

### Uninstall

```shell
sed -i.bak '/\bmise\b/d' ~/.bashrc
```

```shell
sudo rm -rf /usr/local/bin/mise
```

### Update

Update `mise` version:
```shell
mise self-update -y
```

### Cache

```shell
mise cache clear
```

### Settings

```shell
mise settings set experimental true
```

### Manage Tools

Search for a tool in the registry:
```shell
mise search <tool>
```

List installed and active tools:
```shell
mise ls
```

Gets information about a tool:
```shell
mise tool python
```

List outdated tools:
```shell
mise outdated
```

Upgrade all outdated tools:
```shell
mise upgrade
```

Upgrade a specific tool:
```shell
mise upgrade <tool>
```

Install a specific tool:
```shell
mise install <tool>
```

Remove a specific tool:
```shell
mise uninstall <tool>
```

Remove installed tool from mise.toml:
```shell
mise unuse <tool> -y
```

Display the installation path for a tool:
```shell
mise where <tool>
```

Run a command with a specific tool:
```shell
mise x node@25 -- node --version
```

### Tools

Install `node`:
```shell
mise use -g node
```

Install `mermaid-cli`:
```shell
mise use -g npm:@mermaid-js/mermaid-cli
```

Install `aws-cli`:
```shell
mise use -g aws-cli
```

### Config

```shell
# full
mise config ls

# alias
mise cfg ls
```

```shell
mise cfg set tools.deno latest
```

```shell
mise ls -c -J -l
```

```shell
mise bin-paths
```

### Doctor

```shell
mise doctor
```

```shell
mise doctor path
```
