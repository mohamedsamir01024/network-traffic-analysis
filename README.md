# Network Traffic Analysis Lab

## Objective
Analyze network traffic in a controlled lab to identify potentially suspicious behavior and document evidence with mitigation recommendations.

## Lab Setup
- Attacker: Kali Linux (`192.168.7.128`)
- Victim: Metasploitable (`192.168.7.129`)
- Interface: `eth0`
- Protocol Focus: SSH (`TCP/22`)
- Tool: Wireshark

## Key Evidence
- TCP 3-way handshake observed:
  - `SYN` from `192.168.7.128:59674` to `192.168.7.129:22`
  - `SYN,ACK` response from victim
  - `ACK` from attacker
- Terminal proof of successful SSH session.

## Security Interpretation
In real production environments, this pattern can indicate unauthorized remote access if the source host is untrusted or outside policy.

## Mitigation
- Restrict SSH via IP allowlisting
- Enforce strong authentication
- Centralized logging and alerting
- Network segmentation and host hardening

## Repository Contents
- `report/` full report (DOCX/PDF)
- `screenshots/` packet evidence
- `video/` demo recording
