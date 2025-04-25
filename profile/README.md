Gerard Braad's VSCode & VSCodium related repositories
=====================================================

These repositories provide instructions and extensions for use with [VS Code](https://github.com/microsoft/vscode), [VS Codium](https://github.com/VSCodium/) or other code-based editors (Cursor, Windsurf, GitPod, CodeSandbox), and extension API compatible, like [Theia](https://github.com/eclipse-theia/theia).


## Instructions

### Run [`code` and `codium-server` as systemd](https://github.com/gbraad-vscode/code-systemd) services

How to run `code serveweb`, `code tunnel` and `codium-server` as systemd services


## Extensions

### WIP [systemd Universal Manager](https://github.com/gbraad-vscode/systemd-services-manager) - [Marketplace](https://marketplace.visualstudio.com/items?itemName=gbraad.systemd-universal-manager), [Open VSX Registry](https://open-vsx.org/extension/gbraad/systemd-universal-manager)

A Visual Studio Code extension designed to help users manage and maintain the state of systemd services and units on their host systems. 

```json
    "customizations": {
        "vscode": {
            "extensions": [
                ...,
                "gbraad.systemd-universal-manager"
            ]
        }
    }
```


### [Dotfiles checker](https://github.com/gbraad-vscode/dotfiles-checker/) - [Marketplace](https://marketplace.visualstudio.com/items?itemName=gbraad.dotfiles-checker), [Open VSX Registry](https://open-vsx.org/extension/gbraad/dotfiles-checker)

An extension that checks for and install my personal dotfiles


### [Dotfiles tools](https://github.com/gbraad-vscode/dotfiles-tools/) - [Marketplace](https://marketplace.visualstudio.com/items?itemName=gbraad.dotfiles-tools), [Open VSX Registry](https://open-vsx.org/extension/gbraad/dotfiles-tools)

An extension that automates `devenv.zsh` and `machine.zsh`.


### [Extension pack](https://github.com/gbraad-vscode/extension-pack) - [Marketplace](https://marketplace.visualstudio.com/items?itemName=gbraad.extension-pack), [Open VSX Registry](https://open-vsx.org/extension/gbraad/extension-pack)


## devcontainer Features

### Dotfiles

Install my personal dotfiles as a feature during the devcontainer build process.

```json
    "features": {
        "ghcr.io/gbraad-dotfiles/devcontainer-features/dotfiles:latest": {}
    }
```

### Tailscale

Install Tailscale during the devcontainer build process.

```json
    "features": {
        "ghcr.io/gbraad-vscode/devcontainer-features/tailscale:latest": {}
    }
```

After which it is possible to use `tailscale up`.


### cloudflared
```json
    "features": {
        "ghcr.io/gbraad-vscode/devcontainer-features/cloudflared:latest": {}
    }
```

### ssh-keys 
```json
    "features": {
        "ghcr.io/gbraad-vscode/devcontainer-features/ssh-keys:latest": {
            "username": "gbraad"
        }
    }
```


### Run with `systemd`-enabled

To know how to run devcontainers on CodeSpaces with `systemd` enabled, have a look here: https://github.com/orgs/community/discussions/68954#discussioncomment-11812864


## GitHub Actions

### [Codium Server action](https://github.com/gbraad-actions/codium-server-action)

```yaml
- name: Codium Server
  if: ${{ failure() }}
  uses: gbraad-actions/codium-server-action@v1
```

### [`code-serveweb-action`](https://github.com/gbraad-actions/code-serveweb-action)

```yaml
    - name: Code serve web
      if: ${{ failure() }}
      uses: gbraad-actions/code-serveweb-action@v1
```

### [`code-tunnel-action`](https://github.com/gbraad-actions/code-tunnel-action)

```yaml
    - name: Code tunnel
      if: ${{ failure() }}
      uses: gbraad-actions/code-tunnel-action@v1
```
