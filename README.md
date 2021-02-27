# Stack Upload Action

This action runs `stack upload`, typically in response to a tag being pushed.

## Usage

```yaml
name: Release to Hackage

on:
  push:
    tags:
      - 'v*'

jobs:
  create-release:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: pbrisbin/stack-upload-action@main
        with:
          hackage-username: ${{ secrets.HACKAGE_USERNAME }}
          hackage-password: ${{ secrets.HACKAGE_PASSWORD }}
```

## Inputs

See `action.yml`.

## Outputs

None

---

[LICENSE](./LICENSE) | [CHANGELOG](./CHANGELOG.md)
