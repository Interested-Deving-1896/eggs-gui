[update-readmes]   Mode: rewrite — migrating to template structure...
# eggs-gui

[![Built with Ona](https://ona.com/build-with-ona.svg)](https://app.ona.com/#https://github.com/Interested-Deving-1896/eggs-gui)

<!-- AI:start:what-it-does -->
This project provides a unified graphical user interface (GUI) for managing and interacting with Penguins-Eggs, a tool for creating and customizing Linux live systems. It integrates multiple components, including a Go-based daemon, a BubbleTea terminal UI, a NodeGUI desktop application, and a NiceGUI web frontend. It is used by developers and system administrators to streamline tasks such as ISO building, configuration generation, and diagnostics.
<!-- AI:end:what-it-does -->

## Architecture

<!-- AI:start:architecture -->
The project consists of four primary components: a Go-based daemon, a BubbleTea-powered TUI, a NodeGUI desktop application, and a NiceGUI web frontend. These components interact with each other through the Go daemon, which serves as the central backend service. The TUI, desktop, and web interfaces communicate with the daemon to perform tasks such as diagnostics, ISO building, and configuration management.

The repository is organized as follows:

```plaintext
.
├── bin/                # Compiled binaries for daemon and TUI
├── daemon/             # Go daemon source code
│   └── cmd/            # Daemon entry point
├── tui/                # BubbleTea TUI source code
│   └── cmd/            # TUI entry point
├── desktop/            # NodeGUI desktop application
│   ├── src/            # Source code
│   └── dist/           # Build output
├── web/                # NiceGUI web frontend
│   ├── main.py         # Web server entry point
│   └── requirements.txt # Python dependencies
├── Makefile            # Build and run tasks
├── package.json        # Node.js project configuration
└── README.md           # Project documentation
```

The `Makefile` provides targets to build and run each component individually or together. The `package.json` defines scripts and dependencies for the Node.js-based components.
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
- **build.yml**: Builds the project binaries and packages for all supported platforms. No secrets required.
- **build-x86.yml**: Builds and tests the project for x86 architecture. No secrets required.
- **build-arm64.yml**: Builds and tests the project for ARM64 architecture. No secrets required.
- **deploy-book.yml**: Deploys documentation updates to the project's book repository. Requires `BOOK_DEPLOY_TOKEN`.
- **mirror-orgs-full.yml**: Mirrors repositories from the organization to external platforms. Requires `MIRROR_TOKEN`.
- **sync-to-gitlab.yml**: Synchronizes changes from GitHub to GitLab repositories. Requires `GITLAB_TOKEN`.
- **check-accessibility.yml**: Runs accessibility checks on web assets. No secrets required.
- **labeler.yml**: Automatically applies labels to pull requests based on file changes. No secrets required.
- **release.yaml**: Handles version tagging and release creation. Requires `RELEASE_TOKEN`.
- **rotate-token.yml**: Rotates API tokens used in workflows. Requires `ADMIN_TOKEN`.
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
