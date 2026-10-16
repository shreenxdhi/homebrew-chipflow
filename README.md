# Chipflow Homebrew tap

Install the local RTL-to-GDS workflow manager on Linux:

```sh
brew install shreenxdhi/chipflow/chipflow
chipflow setup
chipflow init counter-demo
chipflow run counter-demo/chipflow.yaml --target sim --wait
```

The formula installs the manager into its own Python environment. EDA tools,
ORFS, and platform data are separate; `chipflow setup` checks them and suggests
installation steps without executing those steps.

This initial beta is built from source and may compile Rust-based Python
dependencies. The tap is not a homebrew/core listing. Linux is the validated host;
macOS is not currently supported by this formula.

Source and documentation: https://github.com/shreenxdhi/chipflow
Release: https://github.com/shreenxdhi/chipflow/releases/tag/v0.1.0

Maintainers generate the pinned resources and archive checksum from the exact
release using scripts/generate_formula.py in the main repository. Formula CI runs
a real source installation and the functional `brew test`.
