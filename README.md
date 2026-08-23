<div align="center">

<img src="nullcry%20logo.png" alt="Nullcry Logo" width="140"/>

# 🛡️ nullcry

**Local-First Endpoint Behavior & Threat Detection**

*Watches how your computer actually behaves — no cloud, no telemetry, no noise.*

[![Platform](https://img.shields.io/badge/platform-Windows-0078D6?logo=windows&logoColor=white)](#)
[![Language](https://img.shields.io/badge/built%20with-Python-3776AB?logo=python&logoColor=white)](#)
[![Privacy](https://img.shields.io/badge/data-100%25%20local-27ae60)](#)
[![Status](https://img.shields.io/badge/status-MVP-8e44ad)](#)
[![License](https://img.shields.io/badge/license-Proprietary-lightgrey)](#license)

</div>

---

## Overview

Most breaches today don't start with an exotic zero-day — they start with a click.
A convincing email, a fake update, a "free tool" download: classic **social
engineering**. **Nullcry** is a lightweight Windows endpoint agent that doesn't try
to read the phishing email — it watches what happens **on the machine right after**
someone is tricked, and catches the technical footprint in real time: a new file, an
odd process, an encoded PowerShell command, a persistence entry, a suspicious outbound
connection.

Everything runs **100% locally**. No backend, no cloud dependency, no data ever leaves
the device.

## ✨ Key Features

- 🕵️ **Six parallel behavioral monitors** — files, processes, network, registry
  persistence, scheduled tasks, and CPU spikes
- 🧮 **Transparent risk-scoring engine** — every event adds weighted points to a
  per-process score instead of firing isolated, context-free alerts
- 🔕 **Quiet by design** — a single Windows toast notification only for confirmed
  danger, throttled to at most once every 90 seconds
- 📊 **Live dashboard** — filterable, real-time event table built with Tkinter
- 🔎 **Full forensic detail on demand** — double-click any event for PID, process
  name, full path, remote IP, country, and full risk breakdown
- 📄 **One-click report export** — clean, print-ready HTML report (Ctrl+P → Save as
  PDF)
- 🌍 **Multilingual interface** — English, العربية, Español, Français, हिन्दी, with
  full RTL support for Arabic
- 🔒 **Zero telemetry** — no network calls, no external services, nothing phones home

## 📸 Screenshots

<div align="center">

### Home Screen
<img src="Screenshot%202026-08-23%20191943.png" alt="Nullcry home screen" width="700"/>

### Live Reports Dashboard
<img src="Screenshot%202026-08-23%20192209.png" alt="Nullcry live dashboard" width="700"/>

### Full Event Details
<img src="Screenshot%202026-08-23%20192452.png" alt="Nullcry event details" width="450"/>

### Confirmed Danger Alert
<img src="Screenshot%202026-08-23%20192356.png" alt="Nullcry confirmed danger alert" width="600"/>

</div>

## 🧠 How It Works

Nullcry runs six lightweight background threads, each watching a layer of the
operating system attackers depend on. Every finding feeds a shared, per-process risk
score rather than being judged in isolation.

| Monitor | Watches | Why it matters |
|---|---|---|
| **File Watcher** | New files in Downloads, Temp, AppData | Where a tricked user's malicious download lands first |
| **Process Monitor** | Unapproved executables, LOLBins, dangerous command lines | Catches "living-off-the-land" techniques post-execution |
| **PowerShell Guard** | Encoded commands, download/bypass/hidden keywords | The most common stage right after a phishing click |
| **Persistence Watcher** | Registry `Run` key changes, new Scheduled Tasks | How malware survives a reboot |
| **Network Sentinel** | Outbound connections from non-official paths | Flags C2 / exfiltration traffic |
| **Resource Monitor** | Sudden, sustained CPU spikes | Surfaces silent background activity |

### From raw event to a clear verdict

```
Event observed → Weighted risk points added → Score compared to thresholds
    → Level assigned & logged → Toast alert only if "Confirmed Danger"
```

| Level | Score range | Meaning |
|---|---|---|
| 🟢 Normal | 0 – 24 | Routine activity, logged for context |
| 🟠 Suspicious | 25 – 64 | Worth a glance, not yet alarming |
| 🔴 Risk | 65 – 94 | Multiple weighted factors compounding |
| 🟣 **Confirmed Danger** | 95+ | Only tier that triggers a desktop alert |

## 🚀 Getting Started

### Requirements

```bash
pip install psutil pillow
```

> Requires Windows (uses `winreg`, `schtasks`, and Windows Toast notifications).
> Python 3.9+ recommended.

### Run from source

```bash
python agent.py
```

### Build a standalone executable

```bash
pyinstaller --onefile --noconsole --clean --windowed agent.py
```

The compiled agent registers itself in `HKCU\...\Run` for auto-start and writes logs
to `nullcry_monitor.log` next to the executable.

## 🗺️ Roadmap

- [ ] Benchmark detection accuracy against red-team / phishing simulation datasets
- [ ] Optional encrypted fleet dashboard (raw data still stays on-device)
- [ ] macOS and Linux endpoint support
- [ ] Publish auditable, versioned detection rules
- [ ] Formal packaging & installer for enterprise pilots

## ⚠️ Disclaimer

Nullcry is under active development and provided **as-is**. It is a heuristic,
rule-based behavioral monitor — not a certified antivirus or EDR replacement. Always
pair it with your organization's existing security stack and follow your local
regulations regarding endpoint monitoring and employee privacy.

## 📄 License

Proprietary. All rights reserved. See repository for current licensing terms —
contact the author for commercial use or licensing inquiries.

## 👤 Author

**Omar Zahouri**
📍 Morocco
📧 [ozahouri30@gmail.com](mailto:ozahouri30@gmail.com)
🐙 [github.com/omarzahouri771-creator/NullCry](https://github.com/omarzahouri771-creator/NullCry)

---

<div align="center">
<sub>Built solo, from scratch, in Morocco 🇲🇦 — because effective security tooling doesn't need the cloud to be powerful.</sub>
</div>
