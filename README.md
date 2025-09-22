# Network-Scan-Assessment
A GitHub repository template for documenting Port Analysis and MITRE ATT&amp;CK Mapping based on identified open ports. This repo is structured for SOC/security teams to document reconnaissance findings, risks, and remediation in a clean and formatted way.

# README
* **Purpose:** Document open port analysis and align findings with MITRE ATT&CK techniques for better SOC visibility.
* **Disclaimer:** Only analyze ports/services of systems you own or are authorized to test. Unauthorized scanning is illegal and unethical.
* **Includes:**
   * Open port/service enumeration
   * MITRE ATT&CK technique mapping
   * Risk assessment and remediation templates
 
# Screenshot
<img width="990" height="498" alt="Nmapscan" src="https://github.com/user-attachments/assets/635154b3-fd05-491f-9b31-b861788abcca" />

# Wireshark Packet Capture
<img width="1000" height="626" alt="packetcapture" src="https://github.com/user-attachments/assets/f7c64493-7a97-4971-97e5-a032117f73ec" />

# Example: port-analysis/open_ports.md
## Open Ports Identified
<img width="946" height="448" alt="open ports" src="https://github.com/user-attachments/assets/357227fd-c148-425f-bfb8-c2099dd7ce78" />

# Example: port-analysis/mitre_mapping.md
## MITRE ATT&CK Mapping
<img width="900" height="676" alt="MITRE ATT CK Mapping" src="https://github.com/user-attachments/assets/bc3be277-cf90-496b-8e2b-9f6e99ca7ccb" />

# Example: reports/SOC_risk_report.md
## Executive Summary
A reconnaissance scan revealed multiple open ports on the target environment. Critical services (e.g., SMB on 445) expose the environment to wormable exploits (e.g., EternalBlue) and ransomware. Medium-risk ports include VMware services (902, 912) and web apps (8000, 8089) that may expose sensitive admin panels. Immediate remediation is recommended.

## Findings Summary

 * **High/Critical:** Ports 135, 139, 445 (Windows networking)

* **Medium:** Ports 902, 912 (VMware), 8000, 8089 (web apps)

## Recommendations

* Block external access to SMB (135, 139, 445) at perimeter.

* Disable legacy protocols (SMBv1, NetBIOS).

* Restrict VMware services (902, 912) to management VLAN/VPN.

* Harden web apps (8000, 8089) with strong auth + patching.

* Regular vulnerability scanning and patch cycle.
