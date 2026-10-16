# Chipflow Homebrew tap

Install the stable Chipflow 1.1 release on Linux:

```sh
brew install shreenxdhi/chipflow/chipflow
chipflow setup
chipflow quickstart first-chip
chipflow guide
```

For native Tcl customization:

```sh
chipflow init custom-chip --expert
chipflow hooks
chipflow variables --search clock
```

The browser offers Learning and Expert modes, including a complete YAML copy
editor. Tcl bundles and declared library files are preserved with each run.

The first installation builds dependencies from source and can take several minutes.
Chipflow checks prerequisites and suggests EDA tools; it does not install EDA binaries
or licensed platform data. The supported execution model is single-user local Linux.
See the [operations guide](https://github.com/shreenxdhi/chipflow/blob/main/docs/OPERATIONS.md).

To upgrade, wait for running jobs and back up your history:

```sh
chipflow backup chipflow-history-before-upgrade.tar.gz
brew update
brew upgrade shreenxdhi/chipflow/chipflow
```

The formula pins source archives and SHA-256 checksums, uses a private Python
virtual environment, and has an installed CLI/project/backup/restore test. CI
installs the formula from source and runs `brew test`. This is a third-party tap;
it is separate from homebrew/core.

Source: https://github.com/shreenxdhi/chipflow
Releases: https://github.com/shreenxdhi/chipflow/releases
