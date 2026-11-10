# tinkershell releases

Public command-line binary previews for [tinkershell](https://tinkershell.io):
your persistent agents and tmux sessions, together in the terminal, browser,
iPhone and iPad.

The application source repository remains private while development continues.
This repository contains release documentation and compiled artifacts. Its GitHub
source archives contain this documentation, not the private application source.

## Install

Install the components you need, as the user who owns your sessions:

```sh
curl -fsSL https://tinkershell.io/install-server.sh | bash
curl -fsSL https://tinkershell.io/install-tui.sh | bash
# Optional gateway; configure before starting.
curl -fsSL https://tinkershell.io/install-gateway.sh | bash
```

Default installs live under `~/.local` and need no sudo. Linux uses user systemd
services; macOS uses LaunchAgents. Existing user service settings are preserved.
Use `--system-package` explicitly if you prefer Debian/Ubuntu packages.

The [installation guide](https://tinkershell.io/docs/install.html) explains local
and SSH connections, configuration, version pinning, download-only use and
per-user portable installs. Scripts can be downloaded and inspected first.

- Linux x86_64 and arm64: glibc 2.35+, Debian/Ubuntu packages and portable archives.
- macOS Apple silicon and Intel: macOS 15+, per-user archives and LaunchAgents.
- Host artifacts include a private tmux 3.8 runtime. System tmux is unchanged.
- iPhone/iPad builds are distributed separately from these command-line assets.

See the [latest release](https://github.com/chet/tinkershell-release/releases/latest)
for downloads, `manifest.tsv` and `SHA256SUMS`. Installers verify SHA-256 and byte
length over HTTPS before installation. Explicit Debian packages are registered with dpkg;
there is no apt repository yet, so rerun the installer for a new version.

Ordinary daemon restarts preserve tmux panes and native agent conversations.
Private configuration and provider credentials are not included in release
artifacts. Release notes explain any separate agent-side refresh requirements.

The project is MIT licensed; bundled third-party notices ship with each component.
