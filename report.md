# Network Discovery Report
**Date:** 2025-11-09 
**Network scope:** 192.168.29.0/24 
**Scanning host:** 192.168.29.178 (eth0)

## Summary
Total hosts discovered: 6
Top findings:
1. Router admin interface reachable on 80/443 — default creds risk.
2. IoT device (Espressif) reachable on 80 — no network segmentation.
3. Ubuntu server running outdated Apache — update recommended.

## Methodology
Tools: arp-scan, nmap, awk, curl
Commands run (high level):
- `sudo arp-scan --localnet`
- `sudo nmap -sn 192.168.29.0/24 -oG scans/ping-scan.gnmap`
- `for ip in $(cat scan/live-ips.txt); do sudo nmap -sS -sV -O -p- --open -oA scans/scan_$ip $ip; done`

## Recommendations
- Change default router admin credentials and enable admin over HTTPS only.
- Move IoT devices to a guest/VLAN network with no access to internal hosts.

## Appendix
- `inventory.csv` — full device inventory.
- `scan/` — raw scan outputs for reproducibility.
