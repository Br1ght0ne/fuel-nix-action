# fuel-nix-action

Install Fuel toolchain using fuel.nix. Heavily based on [dtolnay's `rust-toolchain` action](https://github.com/dtolnay/rust-toolchain).

## Example workflow

```yaml
jobs:
  build-forc-project:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: Br1ght0ne/fuel-nix-action@main
      - run: forc build
```

## Inputs

All inputs are optional.

<table>
<tr>
  <th>Name</th>
  <th>Description</th>
</tr>
<tr>
  <td><code>components</code></td>
  <td>Comma-separated string of (optionally versioned) components to install e.g. <code>fuel@nightly, forc@0.19.2, fuel-core</code>. Defaults to <code>fuel</code>. See available components at [fuel.nix book](  https://nix.fuel.network/packages.html#packages).</td>
</tr>
</table>

## License

The scripts and documentation in this project are released under the [MIT
License].

[MIT License]: LICENSE
