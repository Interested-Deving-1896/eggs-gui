[update-readmes]   Mode: rewrite — migrating to template structure...
# eggs-gui

[![Built with Ona](https://ona.com/build-with-ona.svg)](https://app.ona.com/#https://github.com/Interested-Deving-1896/eggs-gui)

<!-- AI:start:what-it-does -->
This project provides a unified graphical user interface (GUI) for managing the penguins-eggs system, combining multiple components: a Go-based daemon, a BubbleTea terminal user interface (TUI), a NodeGUI desktop application, and a NiceGUI web frontend. It simplifies interaction with penguins-eggs for developers and system administrators by offering multiple access points tailored to different use cases and environments.
<!-- AI:end:what-it-does -->

## Architecture

<!-- AI:start:architecture -->
The project consists of four main components that interact to provide a unified GUI for penguins-eggs:

1. **Daemon**: A Go-based backend service (`eggs-daemon`) that handles core operations. It must be running for other components to function.
2. **TUI**: A terminal-based user interface built with BubbleTea (`eggs-tui`) that communicates with the daemon.
3. **Desktop**: A desktop GUI built using NodeGUI. It requires the daemon to be running and uses `npm` for building and running.
4. **Web**: A web-based frontend built with NiceGUI. It requires Python and the daemon to be running.

The components communicate with the daemon, which acts as the central service. The TUI, desktop, and web interfaces interact with the daemon to perform operations and display results.

Directory structure:
```plaintext
.
├── assets/          # Static assets (e.g., icons, desktop files)
├── daemon/          # Go daemon source code
├── desktop/         # NodeGUI desktop application
├── locales/         # Localization files
├── proto/           # Protocol buffer definitions
├── scripts/         # Utility scripts
├── tui/             # BubbleTea TUI source code
├── web/             # NiceGUI web frontend
├── Makefile         # Build and run tasks
├── LICENSE          # License file
├── README.md        # Project documentation
└── ARCHITECTURE.md  # Detailed architecture documentation
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
The repository uses GitHub Actions for continuous integration and automation. Below are the workflows and their purposes:

- **add-mirror-repo.yml**: Adds new repositories to the mirror list.
- **check-gitlab-sync.yml**: Verifies synchronization status between GitHub and GitLab.
- **cleanup-pollution.yml**: Removes unnecessary files or artifacts from the repository.
- **mirror-orgs-full.yml**: Mirrors all repositories from an organization to another.
- **mirror-orgs-watchdog.yml**: Monitors and ensures ongoing synchronization of mirrored organizations.
- **mirror-osp-to-gitlab.yml**: Mirrors open-source projects to GitLab.
- **mirror-releases.yml**: Syncs release artifacts across repositories.
- **pr-automation.yml**: Automates pull request labeling and merging.
- **rate-limit-status.yml**: Monitors API rate limits and logs usage.
- **sync-eggs-docs-to-book.yml**: Syncs documentation to the project’s book format.
- **sync-to-gitlab.yml**: Syncs changes from GitHub to GitLab repositories.
- **token-health.yml**: Checks the validity and expiration of authentication tokens.
- **update-readmes.yml**: Updates README files across repositories.

Required secrets:
- `GITHUB_TOKEN`: Default token for repository access.
- `GITLAB_TOKEN`: Token for GitLab API access.
- `MIRROR_API_KEY`: Key for external mirroring services.
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
[@Interested-Deving-1896](https://github.com/Interested-Deving-1896): 368 commits
<!-- AI:end:contributors -->

## Origins

<!-- AI:start:origins -->
_Original project — no upstream fork._
<!-- AI:end:origins -->

## Resources

<!-- AI:start:resources -->
| File | Description |
|---|---|
| [.gitlab/merge_request_templates/Default.md](https://github.com/Interested-Deving-1896/eggs-gui/blob/main/.gitlab/merge_request_templates/Default.md) | GitLab MR template |
| [config/gitlab-subgroups.yml](https://github.com/Interested-Deving-1896/eggs-gui/blob/main/config/gitlab-subgroups.yml) | GitLab subgroup map |
<!-- AI:end:resources -->

## License

<!-- AI:start:license -->
[MIT](https://github.com/Interested-Deving-1896/eggs-gui/blob/master/LICENSE) © 2026 [Interested-Deving-1896](https://github.com/Interested-Deving-1896)
<!-- AI:end:license -->
