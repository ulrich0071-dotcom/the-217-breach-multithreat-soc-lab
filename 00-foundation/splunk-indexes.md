# Splunk Indexes to Create

Create these indexes in Splunk (Settings → Indexes → New Index), or via CLI.

- `winsec`        — Windows Security
- `sysmon`        — Sysmon Operational
- `powershell`    — PowerShell Operational
- `linuxauth`     — /var/log/auth.log
- `linuxsyslog`   — /var/log/syslog

CLI examples:
```
splunk add index winsec
splunk add index sysmon
splunk add index powershell
splunk add index linuxauth
splunk add index linuxsyslog
```
