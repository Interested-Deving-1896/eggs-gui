[update-readmes]   Mode: rewrite — migrating to template structure...
# eggs-gui

[![Built with Ona](https://ona.com/build-with-ona.svg)](https://app.ona.com/#https://github.com/Interested-Deving-1896/eggs-gui)

<!-- AI:start:what-it-does -->
This project provides a unified graphical user interface (GUI) for managing and interacting with the Penguins-Eggs system. It integrates multiple components, including a Go-based daemon, a BubbleTea terminal UI, a NodeGUI desktop application, and a NiceGUI web frontend. It is designed for users who need tools for diagnostics, ISO building, configuration generation, and accessing a knowledge base in Linux live-system environments.
<!-- AI:end:what-it-does -->

## Architecture

<!-- AI:start:architecture -->
The project consists of four main components: a Go-based daemon, a BubbleTea TUI, a NodeGUI desktop application, and a NiceGUI web frontend. The Go daemon handles core backend operations and serves as the central communication hub. The TUI, desktop, and web interfaces interact with the daemon to provide user-facing functionality. The TUI is a terminal-based interface, the desktop app offers a graphical interface using NodeGUI, and the web frontend is built using Python and NiceGUI.

The repository is organized as follows:

```plaintext
.
├── bin/                # Compiled binaries for daemon and TUI
├── daemon/             # Go daemon source code
│   └── cmd/            # Command-line entry points for the daemon
├── tui/                # BubbleTea TUI source code
│   └── cmd/            # Command-line entry points for the TUI
├── desktop/            # NodeGUI desktop application
├── web/                # NiceGUI web frontend
├── proto/              # Protocol buffer definitions
├── configs/            # Configuration files
├── assets/             # Static assets (e.g., icons, desktop files)
├── doc/                # Documentation
└── Makefile            # Build and run commands
```

Each interface requires the daemon to be running for full functionality. The Makefile provides targets to build and run individual components or the entire system.
<!-- AI:end:architecture -->

## Install

<!-- Add installation instructions here. This section is yours — the AI will not modify it. -->

```bash
git clone https://github.com/Interested-Deving-1896/eggs-gui.git
cd eggs-gui
```

## Usage

<!-- Add usage examples here. This section is yours — the AI will not modify it. -->

## Configuration

<!-- Document configuration options here. This section is yours — the AI will not modify it. -->

## CI

<!-- AI:start:ci -->
The repository uses GitHub Actions for continuous integration and automation. Below are the key workflows:

- **build.yml**: Builds and tests the project for all supported platforms. No secrets required.
- **build-x86.yml**: Builds the project specifically for x86 architecture. No secrets required.
- **build-arm64.yml**: Builds the project specifically for ARM64 architecture. No secrets required.
- **ci.yaml**: Runs linting, unit tests, and integration tests. No secrets required.
- **deploy-book.yml**: Deploys documentation to the web. Requires `DOCS_DEPLOY_TOKEN` secret.
- **mirror-artifacts.yml**: Mirrors build artifacts to external storage. Requires `MIRROR_STORAGE_KEY` secret.
- **sync-to-gitlab.yml**: Syncs the repository to GitLab. Requires `GITLAB_TOKEN` secret.
- **release.yaml**: Automates version tagging and release creation. Requires `RELEASE_TOKEN` secret.
- **check-accessibility.yml**: Runs accessibility checks on documentation and web assets. No secrets required.
- **cleanup-pollution.yml**: Cleans up stale or unused resources in the repository. No secrets required.
<!-- AI:end:ci -->

## Mirror chain

<!-- AI:start:mirror-chain -->
This repo is maintained in [`Interested-Deving-1896/eggs-gui`](https://github.com/Interested-Deving-1896/eggs-gui) and mirrored through:

```
Interested-Deving-1896/eggs-gui  ──►  OpenOS-Project-OSP/eggs-gui  ──►  OpenOS-Project-Ecosystem-OOC/eggs-gui
```

Changes flow downstream automatically via the hourly mirror chain in
[`fork-sync-all`](https://github.com/Interested-Deving-1896/fork-sync-all).
Direct commits to OSP or OOC are detected and opened as PRs back to `Interested-Deving-1896`.
<!-- AI:end:mirror-chain -->

## Contributors

<!-- AI:start:contributors -->
[@Interested-Deving-1896](https://github.com/Interested-Deving-1896): 838 commits

Note: This repository is a mirror. Please refer to the upstream source for additional context.
<!-- AI:end:contributors -->

## Origins

<!-- AI:start:origins -->
_Original project — no upstream fork._
<!-- AI:end:origins -->

## Resources

<!-- AI:start:resources -->
_No additional resource files found._
<!-- AI:end:resources -->

## License

<!-- AI:start:license -->
<!-- License not detected — add a LICENSE file to this repo. -->
<!-- AI:end:license -->
