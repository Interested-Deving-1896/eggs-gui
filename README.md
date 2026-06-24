[update-readmes]   Mode: rewrite — migrating to template structure...
# eggs-gui

[![Built with Ona](https://ona.com/build-with-ona.svg)](https://app.ona.com/#https://github.com/Interested-Deving-1896/eggs-gui)

<!-- AI:start:what-it-does -->
This project provides a unified graphical user interface (GUI) for managing and interacting with Penguins-Eggs, a tool for creating and customizing Linux live systems. It integrates multiple components, including a Go-based daemon, a BubbleTea terminal UI, a NodeGUI desktop application, and a NiceGUI web frontend. It is designed for developers and system administrators who need streamlined tools for diagnostics, ISO building, configuration generation, and accessing a knowledge base.
<!-- AI:end:what-it-does -->

## Architecture

<!-- AI:start:architecture -->
The project consists of four primary components: a Go-based daemon, a BubbleTea TUI, a NodeGUI desktop application, and a NiceGUI web frontend. The Go daemon acts as the backend service, handling core operations and serving as the central communication hub. The TUI, desktop, and web interfaces interact with the daemon to provide different user interfaces for managing penguins-eggs functionalities. The TUI and desktop components are built using Go and Node.js, respectively, while the web frontend is implemented in Python.

The repository is organized as follows:

```plaintext
.
├── bin/                  # Compiled binaries for the daemon and TUI
├── daemon/               # Go daemon source code
│   └── cmd/              # Command-line entry points for the daemon
├── tui/                  # BubbleTea TUI source code
│   └── cmd/              # Command-line entry points for the TUI
├── desktop/              # NodeGUI desktop application source code
├── web/                  # NiceGUI web frontend source code
├── assets/               # Static assets (e.g., icons, desktop files)
├── configs/              # Configuration files
├── proto/                # Protocol buffer definitions
├── Makefile              # Build and run commands
└── package.json          # Node.js metadata and scripts
```

Each component can be built and run independently or together using the `Makefile`. The daemon must be running for the TUI, desktop, and web interfaces to function.
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
The repository uses GitHub Actions for continuous integration and automation. The following workflows are defined:

- `build.yml`: Builds the project binaries and artifacts for supported platforms. No secrets required.
- `test.yml`: Runs unit tests using Vitest. No secrets required.
- `lint.yml`: Executes ESLint to check code quality. No secrets required.
- `deploy.yml`: Deploys the web frontend and desktop application. Requires `DEPLOY_KEY` secret for authentication.
- `mirror-orgs-watchdog.yml`: Monitors and syncs organization repositories. Requires `GH_TOKEN` secret for API access.
- `release.yml`: Handles versioning and publishing of releases. Requires `NPM_TOKEN` secret for publishing to the registry.

Secrets must be configured in the repository settings to enable workflows requiring authentication.
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
[@Interested-Deving-1896](https://github.com/Interested-Deving-1896) - 789 commits

Note: This repository is a mirror. Please refer to the upstream source for the original project.
<!-- AI:end:contributors -->

## Origins

<!-- AI:start:origins -->
_Original project — no upstream fork._
<!-- AI:end:origins -->

## Resources

<!-- AI:start:resources -->
| File | Description |
|---|---|
| [config/gitlab-subgroups.yml](https://github.com/Interested-Deving-1896/eggs-gui/blob/main/config/gitlab-subgroups.yml) | GitLab subgroup map |
<!-- AI:end:resources -->

## License

<!-- AI:start:license -->
<!-- License not detected — add a LICENSE file to this repo. -->
<!-- AI:end:license -->
