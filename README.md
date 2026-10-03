<div align="center">
  <img src="https://tuquet.github.io/icons/scoop-bucket.svg" width="76" height="76" alt="Scoop Bucket Logo" />
  <h1>Scoop Bucket</h1>
  <p><strong>Official Package Manager Distribution Channel for Tuquet Software</strong></p>

  <p>
    <a href="https://scoop.sh"><img src="https://img.shields.io/badge/Scoop-Bucket-brightgreen.svg" alt="Scoop" /></a>
    <img src="https://img.shields.io/badge/Manager-Scoop-blue.svg" alt="Scoop" />
    <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-blue.svg" alt="License" /></a>
  </p>
</div>

---

Official [Scoop](https://scoop.sh) bucket for installing, running, and updating automation ecosystem tools, developer CLIs, and AI agent runtime software.

## 📦 Installation & Setup

Add the Tuquet bucket to your local Scoop installation:

```console
# Add the Tuquet bucket
scoop bucket add tuquet https://github.com/tuquet/scoop-bucket

# Update local bucket index
scoop update
```

---

## 📄 Available Manifests

| Package | Version | Description | Binaries |
| :--- | :---: | :--- | :--- |
| **`claude-agy`** | `7.3.17` | Claude Code CLI with Google Antigravity OAuth integration (Zero API token cost & On-Demand Proxy Lifecycle) | `claude-agy` |
| **`tuquet`** | `1.0.0` | Tuquet Unified Master CLI & Distributed Automation Engine (includes Runner & Automa subsystems) | `tuquet` |

---

## ⚡ Quick Start

### 1. Claude-Agy (`claude-agy`)

Run Anthropic's Claude Code CLI powered by Google Antigravity OAuth quotas:

```console
# 1. Install
scoop install claude-agy

# 2. Launch Claude-Agy
claude-agy

# 3. Switch models dynamically inside Claude chat
/model

# 4. Update anytime
scoop update claude-agy

# 5. Uninstall cleanly
scoop uninstall claude-agy
```

#### Key Features:
- **On-Demand Proxy Lifecycle**: Automatically spawns background `cli-proxy-api` on port `8318` when launching, and terminates the process on exit (0 MB residual RAM).
- **Zero Configuration**: Automatically resolves OAuth tokens from Antigravity CLI and Antigravity IDE (`jetski-standalone-oauth-token`).
- **Data Persistence**: Preserves OAuth tokens, configuration (`settings.env`, `config.yaml`), and session history across version updates in `~/scoop/persist/claude-agy`.

---

### 2. Master CLI (`tuquet`)

Unified master CLI, cloud worker, and browser automation engine:

```console
# 1. Install
scoop install tuquet

# 2. Authenticate workstation with Cloud Control Plane (optional)
tuquet login

# 3. Start the daemon worker
tuquet runner start

# 4. Check unified status
tuquet status

# 5. Run a browser workflow
tuquet automa run <workflow.json>

# 6. Update anytime
scoop update tuquet

# 7. Uninstall cleanly
scoop uninstall tuquet
```

---

## 🔄 Automated Updates

This bucket uses [Scoop Excavator](https://github.com/ScoopInstaller/GithubActions) to track upstream releases:
- **`claude-agy`**: Tracks [router-for-me/CLIProxyAPI](https://github.com/router-for-me/CLIProxyAPI) releases.
- **`tuquet`**: Tracks [tuquet/cli](https://github.com/tuquet/cli) releases.

To manually trigger update checks, navigate to the **Actions** tab on GitHub and run the **Excavator (Auto-Update)** workflow.

---

## 🤝 Contributing

Contributions are welcome! To add or update a manifest:
1. Fork this repository.
2. Add your manifest under the [`bucket/`](bucket/) directory.
3. Validate JSON format using:
   ```console
   node -e "fs.readdirSync('bucket').filter(f=>f.endsWith('.json')).forEach(f=>JSON.parse(fs.readFileSync('bucket/'+f))); console.log('Valid JSON.');"
   ```
4. Submit a Pull Request. CI will automatically validate your manifest syntax.

---

## 🌐 Ecosystem

Part of the **Automation & Agent Ecosystem**:

- [Automa](https://github.com/tuquet/automa) — Next-generation browser automation engine & Web Studio.
- [Runner](https://github.com/tuquet/runner) — Universal distributed process supervision engine in Rust.
- [Browser](https://github.com/tuquet/browser) — High-performance isolated Chromium sandbox & stealth automation core.
- [Cloud](https://github.com/tuquet/cloud) — Enterprise cloud orchestration & real-time telemetry control plane.
- [CLI](https://github.com/tuquet/cli) — Developer ergonomic master CLI, interactive REPL & native MCP server.
- [Lib](https://github.com/tuquet/lib) — Monorepo for shared enterprise UI & utilities (`vue-ui`, `vue-table`, `md-export`, `extension-runner`, `lunar`).
- [Scoop Bucket](https://github.com/tuquet/scoop-bucket) — Official Scoop distribution channel for Tuquet software.

---

## 📜 License

This repository is licensed under the [MIT License](LICENSE).

---

<div align="center">
  <samp>
    <a href="https://tuquet.github.io">Portfolio</a> •
    <a href="https://tuquet.github.io/cv">CV &amp; Resume</a> •
    <a href="https://tuquet.github.io/automa">Automa Studio</a> •
    <a href="https://tuquet.github.io/lib">Component Lab</a> •
    <a href="https://github.com/tuquet/scoop-bucket">Scoop Bucket</a>
  </samp>
</div>
