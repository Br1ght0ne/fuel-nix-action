# fuel-nix-action

Install Fuel toolchain using fuel.nix

## Example workflow

```yaml
name: test suite
on: [push, pull_request]

jobs:
  test:
    name: cargo test
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: Br1ght0ne/fuel-nix-action@main
      - run: forc build
```

## Inputs

All inputs are optional (have defaults).

<table>
<tr>
  <th>Name</th>
  <th>Description</th>
</tr>
<tr>
  <td><code>packages</code></td>
  <td>Comma-separated string of packages to install e.g. <code>forc, fuel-core</code></td>
</tr>
<tr>
  <td><code>milestone</code></td>
  <td>Milestone of Fuel toolchain to use e.g. <code>latest</code>, <code>testnet</code>, <code>nightly</code></td>
</tr>
</table>

## License

The scripts and documentation in this project are released under the [MIT
License].

[MIT License]: LICENSE
