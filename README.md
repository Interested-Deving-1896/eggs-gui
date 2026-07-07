[update-readmes]   Mode: rewrite — migrating to template structure...
# eggs-gui

[![Built with Ona](https://ona.com/build-with-ona.svg)](https://app.ona.com/#https://github.com/Interested-Deving-1896/eggs-gui)

<!-- AI:start:what-it-does -->
This project provides a unified graphical user interface (GUI) for managing and interacting with Penguins-Eggs, a tool for creating and customizing Linux live systems and ISOs. It integrates multiple components, including a Go-based daemon, a BubbleTea terminal UI, a NodeGUI desktop application, and a NiceGUI web frontend. It is designed for Linux users and developers who need a streamlined way to perform diagnostics, build ISOs, generate configurations, and access a knowledge base.
<!-- AI:end:what-it-does -->

## Architecture

<!-- AI:start:architecture -->
The project consists of four main components: a Go-based daemon, a BubbleTea-based TUI, a NodeGUI-based desktop application, and a NiceGUI-based web frontend. These components interact with each other through the Go daemon, which serves as the central backend, managing communication and state. The TUI, desktop, and web frontends act as clients, interfacing with the daemon to provide user interaction. The repository is structured as follows:

```plaintext
.
├── bin/                # Compiled binaries for daemon and TUI
├── daemon/             # Go daemon source code
│   ├── cmd/            # Command-line entry points
├── tui/                # BubbleTea TUI source code
│   ├── cmd/            # Command-line entry points
├── desktop/            # NodeGUI desktop application
│   ├── src/            # Source code for the desktop app
│   ├── dist/           # Built desktop app
├── web/                # NiceGUI web frontend
│   ├── main.py         # Entry point for the web app
│   ├── requirements.txt # Python dependencies
├── Makefile            # Build and run tasks
├── package.json        # Node.js project configuration
├── LICENSE             # License file
└── README.md           # Project documentation
```

The `Makefile` provides tasks to build and run each component individually or together. The daemon must be running for the TUI, desktop, and web frontends to function.
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
The repository uses GitHub Actions for continuous integration and deployment. Below are the relevant workflows:

- **build.yml**: Builds the project for all supported platforms. No secrets required.
- **build-x86.yml**: Builds the project specifically for x86 architecture. No secrets required.
- **build-arm64.yml**: Builds the project specifically for ARM64 architecture. No secrets required.
- **ci.yaml**: Runs linting, tests, and other CI checks. No secrets required.
- **deploy-book.yml**: Deploys the documentation to the designated hosting service. Requires `DOCS_DEPLOY_KEY`.
- **mirror-artifacts.yml**: Mirrors build artifacts to external storage. Requires `ARTIFACT_STORAGE_KEY`.
- **sync-to-gitlab.yml**: Syncs the repository to a GitLab mirror. Requires `GITLAB_TOKEN`.
- **release.yaml**: Handles the release process, including tagging and publishing. Requires `GITHUB_TOKEN` and `NPM_TOKEN`.

Refer to the `.github/workflows/` directory for detailed configurations. Ensure required secrets are added to the repository settings before running workflows.
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
<!-- License not detected — add a LICENSE file to this repo. -->
<!-- AI:end:license -->
