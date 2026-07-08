[update-readmes]   Mode: rewrite — migrating to template structure...
# eggs-gui

[![Built with Ona](https://ona.com/build-with-ona.svg)](https://app.ona.com/#https://github.com/Interested-Deving-1896/eggs-gui)

<!-- AI:start:what-it-does -->
This project provides a unified graphical user interface (GUI) for managing and interacting with Penguins-Eggs, a tool for creating and customizing Linux live systems and ISOs. It integrates multiple components, including a Go-based daemon, a terminal user interface (TUI) built with BubbleTea, a desktop application using NodeGUI, and a web interface powered by NiceGUI. It is designed for developers and system administrators who need a streamlined way to perform diagnostics, build ISOs, generate configurations, and access a knowledge base.
<!-- AI:end:what-it-does -->

## Architecture

<!-- AI:start:architecture -->
The project consists of a unified GUI for Penguins-Eggs, combining multiple components: a Go-based daemon, a BubbleTea TUI, a NodeGUI desktop app, and a NiceGUI web frontend. These components interact through a shared backend service (the daemon), which provides core functionality such as diagnostics, ISO building, and configuration management. The TUI, desktop, and web frontends act as clients to the daemon, communicating via APIs or IPC mechanisms.

The repository is structured as follows:

```plaintext
.
├── bin/                # Compiled binaries for daemon and TUI
├── daemon/             # Go-based backend service
├── tui/                # BubbleTea-based terminal UI
├── desktop/            # NodeGUI-based desktop app
├── web/                # NiceGUI-based web frontend
├── proto/              # Protocol definitions for API communication
├── configs/            # Configuration files and templates
├── assets/             # Static assets (e.g., icons, desktop entry files)
├── doc/                # Documentation files
├── Makefile            # Build and run automation
├── package.json        # Node.js project metadata and scripts
└── README.md           # Project overview and usage instructions
```

Each component can be built and run independently or together using the `Makefile`. The daemon must be running for the TUI, desktop, or web frontends to function.
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
- **build.yml**: Builds the project binaries and packages for all supported architectures. No secrets required.
- **build-x86.yml**: Builds the project specifically for x86 architecture. No secrets required.
- **build-arm64.yml**: Builds the project for ARM64 architecture. No secrets required.
- **deploy-book.yml**: Deploys documentation to the project's book site. Requires `DOCS_DEPLOY_KEY` secret.
- **mirror-artifacts.yml**: Mirrors build artifacts to external storage. Requires `MIRROR_STORAGE_KEY` secret.
- **sync-to-gitlab.yml**: Syncs repository changes to GitLab. Requires `GITLAB_TOKEN` secret.
- **check-accessibility.yml**: Runs accessibility checks on the web frontend. No secrets required.
- **labeler.yml**: Automatically applies labels to pull requests based on file changes. No secrets required.
- **release.yml**: Handles version tagging and release creation. Requires `GH_TOKEN` secret.
- **ci.yaml**: Runs unit tests, linting, and integration tests. No secrets required.
- **cleanup-pollution.yml**: Cleans up temporary files and artifacts after CI runs. No secrets required.
- **rotate-token.yml**: Rotates API tokens for external integrations. Requires `TOKEN_ROTATION_KEY` secret.
- **validate-readme-render.yml**: Ensures README formatting and rendering correctness. No secrets required.
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
[@Interested-Deving-1896](https://github.com/Interested-Deving-1896): 859 commits
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
[MIT](https://github.com/Interested-Deving-1896/eggs-gui/blob/master/LICENSE) © 2026 [Interested-Deving-1896](https://github.com/Interested-Deving-1896)
<!-- AI:end:license -->
