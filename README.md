# SOC Home Lab – Threat Detection Environment

A hands-on Security Operations Center (SOC) home lab designed to practice threat detection, security monitoring, log analysis, IOC extraction, and incident investigation.

The environment integrated **pfSense**, **Sysmon**, and **CrowdSec** to provide network and endpoint visibility for analyzing simulated security activity.

---

## Overview

This project documents a practical SOC home lab focused on understanding how security analysts detect, investigate, and analyze suspicious activity using multiple sources of security telemetry.

The lab involved:

- Network security monitoring
- Endpoint telemetry
- Attack simulation
- Security log analysis
- Threat detection
- IOC extraction
- Incident investigation
- Defensive security workflows

---

## Objectives

The main objectives of this lab were to:

- Build a practical SOC-style monitoring environment
- Understand endpoint and network security telemetry
- Generate simulated security activity
- Analyze endpoint and network logs
- Identify suspicious activity
- Extract Indicators of Compromise (IOCs)
- Practice threat detection workflows
- Investigate simulated security incidents
- Understand how multiple telemetry sources support incident investigation

---

## Technologies Used

| Technology | Purpose |
|---|---|
| **pfSense** | Firewall and network security monitoring |
| **Sysmon** | Endpoint telemetry and activity monitoring |
| **CrowdSec** | Threat detection and defensive security |
| **Security Logs** | Investigation and analysis |
| **Attack Simulations** | Generating security-relevant activity |

---

## Lab Architecture

The lab combined network-level and endpoint-level security visibility.

```text
                    Attack Simulation
                           |
                           v
                    Network Activity
                           |
                           v
                     +-----------+
                     |  pfSense  |
                     |  Firewall |
                     +-----------+
                           |
                           |
             +-------------+-------------+
             |                           |
             v                           v
      Network Telemetry          Endpoint Activity
                                         |
                                         v
                                   +-----------+
                                   |  Sysmon   |
                                   +-----------+
                                         |
                                         v
                                  Endpoint Logs

                     +-------------------+
                     |      CrowdSec      |
                     | Threat Detection   |
                     +-------------------+

                           |
                           v
                    Log Investigation
                           |
                           v
                     IOC Extraction
                           |
                           v
                  Incident Investigation
