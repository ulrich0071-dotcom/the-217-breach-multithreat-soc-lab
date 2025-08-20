# VMware Host‑Only Network (example)

- Network: VMnet7 (Host‑Only)
- Subnet: 192.168.217.0/24
- DHCP: enabled (optional)
- Host Splunk IP on VMnet7: 192.168.217.1  (replace with your actual)

> Point your Universal Forwarders to the **host’s** Splunk receiver on this network, e.g., `192.168.217.1:9997`.
