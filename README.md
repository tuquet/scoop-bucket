# 🚀 Tuquet Scoop Bucket

Official [Scoop](https://scoop.sh) bucket for installing and updating Tuquet ecosystem software on Windows.

## 📦 Installation

To add this bucket and install software, run the following commands in PowerShell:

```powershell
# 1. Add the Tuquet bucket
scoop bucket add tuquet https://github.com/tuquet/tuquet-scoop-bucket

# 2. Install Tuquet Automa Engine CLI
scoop install automa
```

## ⚡ Quick Start

After installation, launch the Automa Engine & Web Studio:

```powershell
automa start
```

To update to the latest release anytime:

```powershell
scoop update automa
```

---

## 📄 Manifests in this Bucket

- **`automa`**: Tuquet Automa Engine & Daemon (`automa-core`)
