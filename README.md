# crab-toolchain

Home of the Crab GitHub Toolchain Action

This is an adapted version for Crab [from here](https://github.com/dtolnay/rust-toolchain) - [MIT license](https://github.com/dtolnay/rust-toolchain/blob/master/LICENSE)

## Example workflow

```yaml
name: CI
on: [push, pull_request]

jobs:
  test:
    name: cargo test
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: rinse-repeat/crab-toolchain@main
        with:
          toolchain: stable
      - run: cargo test --all-features
```
