Gerard Braad's VScode related repositories
==========================================


## Instructions

### [`code` as systemd](https://github.com/gbraad-vscode/codecli-systemd)

How to run `code serveweb` and `code tunnel` as systemd services


## Extensions

### WIP [systemd Services Manager](https://github.com/gbraad-vscode/systemd-services-manager)

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

## Features

### Tailscale

```json
    "features": {
        "ghcr.io/gbraad-vscode/devcontainer-features/tailscale:latest": {}
    }
```

After which it is possible to use `tailscale up`.
