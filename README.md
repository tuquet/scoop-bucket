# 🚀 Tuquet Scoop Bucket

Official [Scoop](https://scoop.sh) bucket for installing and updating Tuquet ecosystem software and AI agent tooling on Windows.

## 📦 Installation

To add this bucket and install software, run the following commands in PowerShell:

```powershell
# 1. Add the Tuquet bucket
scoop bucket add tuquet https://github.com/tuquet/tuquet-scoop-bucket

# 2. Install desired application
scoop install claude-agy
```

## ⚡ Quick Start: Claude-Agy (Claude Code + Antigravity OAuth)

Run Anthropic's Claude Code CLI with Google Antigravity OAuth quota (zero API token cost):

```powershell
# Launch Claude-Agy
claude-agy

# Switch models dynamically in chat
/model
```

To update to the latest release anytime:

```powershell
scoop update claude-agy
```

To uninstall cleanly:

```powershell
scoop uninstall claude-agy
```

---

## 📄 Manifests in this Bucket

- **`claude-agy`**: Anthropic Claude Code CLI with Google Antigravity OAuth integration (On-Demand Proxy Lifecycle, Root Sandbox Bypass, Dynamic Model Discovery).
- **`automa`**: Tuquet Automa Engine & Daemon (`automa-core`).
