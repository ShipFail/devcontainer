# Ship.Fail Devcontainer Template

This repo is the **golden devcontainer template** for Ship.Fail projects.

- **Single source of truth** for dev environment defaults (image, tools, editor extensions, etc.).
- Each project **copies** `devcontainer.json` from here into its own `.devcontainer/devcontainer.json`.
- When we upgrade the dev env, we **change it here first**, then selectively refresh projects.

> Mental model: _“If I need to remember anything about devcontainers, I look in `shipfail/devcontainer`.”_

---

## How to use in a new project

Copy it in a Ship.Fail project repo.

```sh
mkdir -p .devcontainer/
curl -o .devcontainer/devcontainer.json \
  https://shipfail.github.io/devcontainer/devcontainer.json

mkdir -p .devcontainer/features/npm-packages
curl -o .devcontainer/features/npm-packages/devcontainer-feature.json \
  https://shipfail.github.io/devcontainer/features/npm-packages/devcontainer-feature.json
curl -o .devcontainer/features/npm-packages/install.sh \
  https://shipfail.github.io/devcontainer/features/npm-packages/install.sh

mkdir -p .devcontainer/features/gh-auto-auth
curl -o .devcontainer/features/gh-auto-auth/devcontainer-feature.json \
  https://shipfail.github.io/devcontainer/features/gh-auto-auth/devcontainer-feature.json
curl -o .devcontainer/features/gh-auto-auth/install.sh \
  https://shipfail.github.io/devcontainer/features/gh-auto-auth/install.sh
curl -o .devcontainer/features/gh-auto-auth/auth-script.sh \
  https://shipfail.github.io/devcontainer/features/gh-auto-auth/auth-script.sh
```

That's it.

## Author

Huan, Dec 8, 2025
