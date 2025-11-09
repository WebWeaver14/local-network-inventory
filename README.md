      
# Local Network Discovery & Device Inventory
Find every device on a local network (phones, printers, cameras, PCs) and make a tidy list of what each device is and what it’s running.

## Scope
- Date: 2025-11-09
- Network (lab/home): 192.168.29.0/24
- Scanning host: 192.168.29.178 (eth0)
- Tools: arp-scan, nmap, awk, curl

## Goal
Produce an inventory CSV of devices and include raw scan outputs for reproducibility.

## Deliverables
- `inventory.csv` — device inventory (IP, MAC, Hostname, Vendor, Open ports, Services, OS_guess, Notes)
- `scans/` — raw nmap outputs (`.nmap`, `.gnmap`, `.xml`) and any arp-scan output
- `report.md` — summary of findings and remediation




