Gerard Braad's VScode related repositories
==========================================


## Extensions

### WIP [systemd Services Manager](https://github.com/gbraad-vscode/systemd-services-manager)

A Visual Studio Code extension designed to help users manage and maintain the state of systemd services and units on their host systems. 

```json
    "customizations": {
        "vscode": {
            "extensions": [
                ...,
                "gbraad.systemd-services-manager"
            ]
        }
    }
```

 - https://open-vsx.org/extension/gbraad/systemd-services-manager
 - https://marketplace.visualstudio.com/items?itemName=gbraad.systemd-services-manager

## Features

### Tailscale

```json
    "features": {
        "ghcr.io/gbraad-vscode/devcontainer-features/tailscale:latest": {}
    }
```

After which it is possible to use `tailscale up`.
