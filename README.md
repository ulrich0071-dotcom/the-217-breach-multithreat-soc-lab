# The 2:17 Breach — Multi‑Threat SOC Lab (Splunk)

From one click to a full breach: **phishing → credential abuse → ransomware → cloud abuse → insider risk**.

This repo contains a reproducible SOC lab: detections, dashboards, playbooks, simulation data, and documentation.
It is organized in phases so you can implement one capability at a time and still keep the full story coherent.

## Tech Stack
- **Splunk** (SIEM) on your host
- **Windows VM** with Sysmon + PowerShell logs
- **Linux VM** (Ubuntu/Debian) with auth/syslog
- Optional: Azure sign-in logs (when available), Kali for attack simulation

## Goals
- Cut noise with correlation, detect faster, respond smarter
- Map detections to **MITRE ATT&CK**
- Produce dashboards + an executive one‑pager per phase

> ⚠️ **No secrets in this repo.** Never commit real IPs, credentials, tokens, or exported private configs.
