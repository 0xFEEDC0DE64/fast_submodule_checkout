# fast_submodule_checkout
GitHub action to update or clone a submodule much faster by enabling caching

## Example workflow

```yaml
name: Getting the hash of the corelib submodule

on: push

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v2

    - name: Fast Submodule Checkout libs/corelib
      uses: 0xFEEDC0DE64/fast_submodule_checkout@main
      with:
        submodule: libs/corelib

    - name: Use corelib
      run: ls -lah libs/corelib
```

