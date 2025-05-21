# Codex Setup Instructions (Anti-Spyware Toolkit)

## Overview
This environment analyzes iOS/macOS system logs and forensic traces for spyware, OTA restore loops, MDM profiles, Siri abuse, and network manipulation.

## Setup Instructions

Paste this into the "Setup Script" box in Codex:
```
pip install -r requirements.txt
bash setup.sh
```

## Required Files in the Repo
- `requirements.txt` — Required Python packages
- `setup.sh` — Creates folders (`logs/`, `output/`, `reports/`)
- `scripts/` — Python tools to parse `.ips`, `.json`, `.plist`, etc.
- `logs/raw_diagnostics/` — Place logs like:
  - `SiriSearchFeedback-*.ips`
  - `OTAUpdate-*.ips`
  - `MessagesAirlockService-*.ips`
  - `JetsamEvent-*.ips`
  - `wifi.log`, `system.log`, `analytics.json`

## After Launching
- Use:
  ```bash
  python scripts/parse_siri_log.py logs/raw_diagnostics/SiriSearchFeedback-2025-05-20.ips
  ```
- Save findings into `/output/` or structured reports

## Reminder
Internet access ends after setup. Make sure all packages and files are in the repo before launching.
