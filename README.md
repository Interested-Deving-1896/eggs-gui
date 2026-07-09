[update-readmes]   Mode: rewrite — migrating to template structure...
# eggs-gui

[![Built with Ona](https://ona.com/build-with-ona.svg)](https://app.ona.com/#https://github.com/Interested-Deving-1896/eggs-gui)

<!-- AI:start:what-it-does -->
This project provides a unified graphical user interface (GUI) for managing and interacting with Penguins-Eggs, a tool for creating and customizing Linux live systems and ISOs. It integrates a Go-based daemon, a BubbleTea terminal user interface (TUI), a NodeGUI desktop application, and a NiceGUI web frontend. It is designed for developers and system administrators who need a streamlined way to perform diagnostics, build ISOs, generate configurations, and access a knowledge base through an AI-powered agent.
<!-- AI:end:what-it-does -->

## Architecture

<!-- AI:start:architecture -->
The project consists of four main components that interact to provide a unified GUI for penguins-eggs:

1. **Go Daemon**: A backend service built with Go, responsible for handling core operations and exposing APIs for other components.
2. **BubbleTea TUI**: A terminal-based user interface built with the BubbleTea framework, communicating with the daemon for command-line interactions.
3. **NodeGUI Desktop**: A desktop application built with NodeGUI, providing a graphical interface for users.
4. **NiceGUI Web**: A web-based frontend built with Python and NiceGUI, offering remote access to the system.

The components communicate with the Go daemon, which acts as the central hub for processing requests and managing system state. The TUI, desktop, and web interfaces connect to the daemon to perform operations and retrieve data.

The repository is organized as follows:

```plaintext
.
├── bin/                # Compiled binaries for the daemon and TUI
├── daemon/             # Go daemon source code
├── tui/                # BubbleTea TUI source code
├── desktop/            # NodeGUI desktop application
├── web/                # NiceGUI web frontend
├── assets/             # Static assets (e.g., icons, desktop files)
├── configs/            # Configuration files
├── doc/                # Documentation
├── Makefile            # Build and run commands
├── package.json        # Node.js metadata for eggs-ai
└── README.md           # Project overview
```
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
The repository uses GitHub Actions for CI/CD workflows. Below is a summary of key workflows and their functions:

- **build.yml**: Builds the project binaries and artifacts for supported platforms. No secrets required.
- **test.yml**: Runs unit tests using `vitest` and checks code quality with `eslint`. No secrets required.
- **deploy.yml**: Deploys the web frontend and desktop application. Requires `DEPLOY_KEY` secret for authentication.
- **mirror-artifacts.yml**: Synchronizes build artifacts with external repositories. Requires `MIRROR_TOKEN` secret.
- **sync-to-gitlab.yml**: Mirrors the repository to GitLab. Requires `GITLAB_TOKEN` secret.
- **check-accessibility.yml**: Validates accessibility compliance for web components. No secrets required.
- **cleanup-pollution.yml**: Cleans up temporary files and stale workflows. No secrets required.
- **release.yml**: Automates version tagging and package publishing. Requires `NPM_TOKEN` secret.

Secrets must be configured in the repository settings for workflows requiring authentication.
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
[@Interested-Deving-1896](https://github.com/Interested-Deving-1896): 870 commits

Note: This repository is a mirror. Please refer to the upstream source for additional contributions and context.
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
