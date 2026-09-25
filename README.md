# 🚀 Tuquet Scoop Bucket

Official [Scoop](https://scoop.sh) bucket for installing, running, and updating Tuquet ecosystem tools and AI agent runtime software on Windows.

---

## 📦 Installation & Setup

Add the Tuquet bucket to your local Scoop installation:

```powershell
# Add the Tuquet bucket
scoop bucket add tuquet https://github.com/tuquet/tuquet-scoop-bucket

# Update local bucket index
scoop update
```

---

## 📄 Available Manifests

| Package | Version | Description | Binaries |
| :--- | :---: | :--- | :--- |
| **`claude-agy`** | `7.3.17` | Claude Code CLI with Google Antigravity OAuth integration (Zero API token cost & On-Demand Proxy Lifecycle) | `claude-agy.cmd` |
| **`automa`** | `1.0.0` | Tuquet Automa Engine - High-performance automation CLI & daemon runtime | `automa.exe` |

---

## ⚡ Quick Start

### 1. Claude-Agy (`claude-agy`)

Run Anthropic's Claude Code CLI powered by Google Antigravity OAuth quotas:

```powershell
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

### 2. Tuquet Automa Engine (`automa`)

Run the Tuquet Automa automation engine and daemon:

```powershell
# 1. Install
scoop install automa

# 2. Start the daemon
automa start

# 3. Update anytime
scoop update automa

# 4. Uninstall
scoop uninstall automa
```

---

## 🔄 Automated Updates

This bucket uses [Scoop Excavator](https://github.com/ScoopInstaller/GithubActions) to track upstream releases:
- **`claude-agy`**: Tracks [router-for-me/CLIProxyAPI](https://github.com/router-for-me/CLIProxyAPI) releases.
- **`automa`**: Tracks [tuquet/tuquet-automa](https://github.com/tuquet/tuquet-automa) releases.

To manually trigger update checks, navigate to the **Actions** tab on GitHub and run the **Excavator (Auto-Update)** workflow.

---

## 🤝 Contributing

Contributions are welcome! To add or update a manifest:
1. Fork this repository.
2. Add your manifest under the [`bucket/`](bucket/) directory.
3. Validate JSON format using:
   ```powershell
   Get-ChildItem -Path bucket\*.json | ForEach-Object { Get-Content $_.FullName | ConvertFrom-Json | Out-Null }
   ```
4. Submit a Pull Request. CI will automatically validate your manifest syntax.

---

## 📜 License

This repository is licensed under the [MIT License](LICENSE).
