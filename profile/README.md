Gerard Braad's VScode related repositories
==========================================


## Instructions

### Run [`code` as systemd](https://github.com/gbraad-vscode/code-systemd) services

How to run `code serveweb` and `code tunnel` as systemd services


## Extensions

### WIP [systemd Universal Manager](https://github.com/gbraad-vscode/systemd-services-manager)

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

 - [Open VSX Registry](https://open-vsx.org/extension/gbraad/systemd-universal-manager)
 - [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=gbraad.systemd-universal-manager)

### [Dotfiles checker](https://github.com/gbraad-vscode/dotfiles-checker/)

An extension that checks for and install my personal dotfiles


### [Dotfiles tools](https://github.com/gbraad-vscode/dotfiles-tools/)

An extension that automates `devenv.zsh` and `machine.zsh`.


## devcontainer Features

### Tailscale

```json
    "features": {
        "ghcr.io/gbraad-vscode/devcontainer-features/tailscale:latest": {}
    }
```

After which it is possible to use `tailscale up`.


### Run with `systemd`-enabled

To know how to run devcontainers on CodeSpaces with `systemd` enabled, have a look here: https://github.com/orgs/community/discussions/68954#discussioncomment-11812864


## GitHub Actions

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
