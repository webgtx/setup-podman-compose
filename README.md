<div align=center>

# Setup Podman Compose
Set up your GitHub Actions workflow with a latest stable podman-compose

</div>

## Usage 

```yaml
name: Podman Comopse Workflow

on:
  push:
    branches: ["master"]

jobs:
  setup:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: webgtx/setup-podman-compose@v1
      - run: podman-compose -f "compose.yml" up -d
```
