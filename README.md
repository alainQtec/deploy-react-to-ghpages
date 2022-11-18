## Build and deploy react to gh-pages

This action will automate the process of building and depolying react app in gh-pages branch.

## INSTALLATION

Copy and paste the following snippet into your .yml file.

```yaml
- name: Deploy react to gh-pages
  uses: alainQtec/deploy-react-to-ghpages@1.0.0-beta.2
```

## Use case Example

Create `build-and-deploy.yml` in [`.github/workflows/`](#/tree/main/.github/workflows)

Set its content to:

```yaml
name: Build and deploy to gh-pages

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  build:

    runs-on: ubuntu-latest
    
    steps:
    - uses: actions/checkout@v2

    - name: Deploy react to gh-pages
      uses: alainQtec/deploy-react-to-ghpages@1.0.0-beta.2
```

That's it!
