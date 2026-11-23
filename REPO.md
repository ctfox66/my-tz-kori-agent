# komari-agent (ctfox66 fork)

Monitoring agent for the Komari server (`ctfox66/my-tz-kori-server`, line `1.2.5-fix2`).

- Base: agent `1.2.13`, remote-control (Web Shell / file manager) removed.
- Self-update and the installers consume **this** repository's releases
  (`update.Repo = ctfox66/my-tz-kori-agent`, install URLs under `ctfox66/my-tz-kori-agent`).
- Releases must use a plain version tag (e.g. `v1.2.14`) so auto-update and the installers can
  resolve them. `.github/workflows/release.yml` attaches `komari-agent-<os>-<arch>` binaries.

## Install

```bash
bash <(curl -fsSL https://raw.githubusercontent.com/ctfox66/my-tz-kori-agent/master/install.sh)
```

Windows: `install.ps1` from the same repo.

## Build

```bash
go build -trimpath -ldflags="-X github.com/komari-monitor/komari-agent/update.CurrentVersion=v1.2.14" .
```
