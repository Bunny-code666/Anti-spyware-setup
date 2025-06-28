#
# Anti-Spyware Diagnostic Environment (ChatGPT + Forensic Logs)

## 1. Overview
This project is a personal AI-assisted anti-spyware lab using ChatGPT with Codex tools to analyze iOS/macOS system behavior. It supports log decoding, OTA restore failure analysis, and embedded surveillance detection.

## 2. Features
- Log file parsing (.ips, .json, .plist)
- Embedded speech service and Siri surveillance detection
- OTA restore anomaly decoding
- HealthKit, backup, and signature mismatch scans
- ChatGPT code analysis and forensic report generation

## 3. Setup & Usage
Run inside ChatGPT with code interpreter:
1. Upload log files
2. Request decoding (e.g., "analyze OTA for restore error")
3. Receive forensic insights

## 4. Contributing
This repository is currently personal. Future contributions may follow a structured model.

## 5. License
Private forensic research use only. Do not distribute logs or personal data without permission.

## 6. Reading sysdiagnose Logs

To analyze sysdiagnose logs (Apple’s comprehensive system reports), upload the `.tar.gz` or `.logarchive` directly into this environment. If you were unable to upload due to size:

- Extract the archive locally using macOS or Linux:
  ```bash
  tar -xzf sysdiagnose_YYYY-MM-DD_xxxxxx.tar.gz
  ```
- Navigate to:
  - `system_logs.logarchive/`
  - or `DiagnosticLogs/`
- Isolate files like `system.log`, `wifi.log`, or `Baseband`
- Then upload specific `.log` or `.plist` files separately

These files may contain key data on:
- Network spoofing
- VPN or proxy routing
- Reboots, restore attempts
- Hardware failures

If needed, compress and upload subsets manually for targeted decoding.


## 7. Advanced Features (Network, Developer Tools, and Pegasus-Style Tracing)

This toolkit is being expanded to detect and trace high-grade digital surveillance, including:

- **Network Monitoring & Proxy Detection**
  - Analyze Wi-Fi logs for rogue gateways or DNS manipulation
  - Identify VPN/proxy hijacking, MAC spoofing, or Evil Twin networks

- **Developer Tool Intrusion**
  - Detect injected profiles used to mimic developer mode (without TestFlight)
  - Scan logs for unauthorized usage of entitlements, sandbox breaches, or Apple Configurator

- **Pegasus-Class Surveillance Clues**
  - Persistent speech/microphone daemons (e.g., Siri abuse)
  - OTA restore failures (signatures `812`, `5`)
  - Trust store manipulations, rogue certificates, backchannel traffic

- **Traceback & Forensic Attribution (Experimental)**
  - Log source correlation via baseband, Wi-Fi logs, and certificate issuers
  - Extract identifiers tied to profile provisioning or MDM-style delivery
  - Create a timeline of digital coercion to support legal reporting

---

## Coming Soon:
- `trace_mdms.py` — Trace rogue device management links
- `scan_wifi_spoof.py` — Detect Evil Twin and MAC relay attacks
- `extract_certchain.py` — Identify unauthorized certs in trust store

To contribute or request custom modules for legal/forensic use, submit a GitHub issue or contact repo owner directly.
