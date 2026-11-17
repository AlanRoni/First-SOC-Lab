# Home SOC Lab

A home security operations lab where I practise the daily work of a Junior SOC analyst: collecting logs, monitoring endpoints, detecting attacks and investigating alerts. I'm building it step by step and documenting each exercise as I finish it.

**Goal:** build practical blue-team skills in SIEM, endpoint monitoring, network security and incident investigation.

## Architecture

```
Windows laptop (host)
 ├─ Wazuh agent ── logs and events ──► Wazuh server + dashboard
 │                                     (Ubuntu VM in VirtualBox)
 ├─ Wireshark (network traffic capture)
 └─ [In progress] pfSense firewall VM
```

## Components and status

| Component | Purpose | Status |
|---|---|---|
| Wazuh server and dashboard (Ubuntu VM, VirtualBox) | SIEM: log collection, alerting, dashboards | Built |
| Wazuh agent on Windows endpoint | Sends endpoint logs and events to the SIEM | Built |
| Wireshark | Network traffic capture and analysis | Installed |
| pfSense | Lab firewall, with its logs reviewed in Wazuh | In progress |
| Windows Defender and Wazuh active response | Endpoint protection testing | In progress |
| Attack simulation and custom detection rule | Practise detection and investigation | Planned |

## Exercises

Each exercise is a short write-up of what I ran, what the alerts looked like, how I investigated and what I learned.

- [ ] Exercise 01: Brute-force logins against the Windows endpoint, with alert investigation and a custom Wazuh rule (planned)
- [ ] Exercise 02: 

## Setup guides

- `docs/setup-wazuh.md`: installing the Wazuh server on Ubuntu
- `docs/setup-agent.md`: enrolling the Windows endpoint
- `docs/setup-pfsense.md`: adding the firewall (coming soon)

## Skills practised

SIEM monitoring (Wazuh) · log analysis · endpoint monitoring · network traffic analysis · firewall basics · detection rule writing · incident investigation

## Environment

- Host: Windows laptop, VirtualBox
- Wazuh version: [4.14.10]
- Ubuntu version: [26.04]

## Security notes

This repo contains documentation, configuration snippets and screenshots only. No VM images, agent keys, credentials or personal details are committed.

## About

Built by Alan Roni Mathew. CompTIA Security+ certified, Dubai, UAE. https://www.linkedin.com/in/alanroni/
