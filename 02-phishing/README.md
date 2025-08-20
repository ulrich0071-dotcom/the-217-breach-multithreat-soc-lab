# Phase 2 — Phishing → Click → Auth Fail

Data:
- `phish:email` from `data/email_log.csv`
- `phish:click` from `data/click_log.csv`

Goal: correlate a malicious click with Windows 4625 failures in the same 5-minute window for the same user.

**Ingest steps** (Splunk):
1. Settings → Indexes → *New Index* → name: `phish` → Save.
2. Settings → Add Data → Upload:
   - Upload `email_log.csv`
     - **Sourcetype:** `phish:email`
     - **Index:** `phish`
     - **Timestamp field:** `time` (format `%Y-%m-%d %H:%M:%S`)
   - Upload `click_log.csv`
     - **Sourcetype:** `phish:click`
     - **Index:** `phish`
     - **Timestamp field:** `time` (format `%Y-%m-%d %H:%M:%S`)

**Queries**
- Emails: `index=phish sourcetype=phish:email | stats count by verdict delivery`
- Clicks:  `index=phish sourcetype=phish:click | stats count by verdict browser`
- Correlation: see `searches/phish-click-to-authfail.spl`
