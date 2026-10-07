# SOC Home Lab Architecture

## Overview

The SOC Home Lab was designed as a controlled environment for practicing security monitoring, threat detection, log analysis, IOC extraction, and incident investigation.

The environment combined network-level visibility through **pfSense** with endpoint telemetry from **Sysmon** and defensive threat detection capabilities provided by **CrowdSec**.

---

## High-Level Architecture

```text
                    +----------------------+
                    |   Attack Simulation  |
                    +----------+-----------+
                               |
                               v
                    +----------------------+
                    |    Network Activity  |
                    +----------+-----------+
                               |
                               v
                    +----------------------+
                    |       pfSense        |
                    | Firewall / Network   |
                    |      Visibility      |
                    +----------+-----------+
                               |
                    +----------+----------+
                    |                     |
                    v                     v
          +----------------+     +------------------+
          | Network        |     | Endpoint         |
          | Telemetry      |     | Activity         |
          +----------------+     +--------+---------+
                                          |
                                          v
                                  +---------------+
                                  |    Sysmon     |
                                  |   Telemetry   |
                                  +-------+-------+
                                          |
                                          v
                                  +---------------+
                                  | Endpoint Logs |
                                  +---------------+

                    +----------------------+
                    |      CrowdSec        |
                    |  Threat Detection    |
                    +----------+-----------+
                               |
                               v
                    +----------------------+
                    |  Security Analysis   |
                    +----------+-----------+
                               |
                               v
                    +----------------------+
                    |   IOC Extraction     |
                    +----------+-----------+
                               |
                               v
                    +-----------------------+
                    | Incident Investigation|
                    +-----------------------+
```

---

## Core Components

### pfSense

pfSense was used as the firewall and network security component of the SOC home lab.

It provided network-level visibility that could be used alongside endpoint telemetry during security monitoring and incident investigation.

### Sysmon

Sysmon was used to provide endpoint telemetry for security monitoring and investigation.

The telemetry provided additional visibility into activity occurring on monitored systems during security exercises.

### CrowdSec

CrowdSec was incorporated as part of the defensive threat detection workflow.

It provided an additional security layer for analyzing suspicious activity within the lab environment.

---

## Telemetry Sources

The lab considered two primary visibility layers:

### Network Telemetry

Network-level activity was observed through the firewall and associated network security information.

### Endpoint Telemetry

Endpoint activity was monitored through Sysmon-generated telemetry.

These different sources provided complementary evidence during security investigations.

---

## Investigation Flow

The different telemetry sources were used together during investigation:

```text
Network Activity
       |
       v
    pfSense
       |
       v
Network Evidence
       |
       +----------------------+
                              |
                              v
                         Correlation
                              ^
                              |
       +----------------------+
       |
    Sysmon
       |
       v
Endpoint Evidence
       |
       v
Log Analysis
       |
       v
IOC Extraction
       |
       v
Incident Investigation
```

---

## Security Operations Workflow

The architecture supported a basic SOC investigation lifecycle:

1. Generate controlled security activity
2. Observe network and endpoint telemetry
3. Review available security logs
4. Identify suspicious activity
5. Correlate available evidence
6. Extract relevant IOCs
7. Investigate the incident
8. Document findings

---

## Detection and Investigation Model

The overall workflow can be summarized as:

```text
Attack Simulation
       |
       v
Security Activity
       |
       v
Network + Endpoint Telemetry
       |
       v
Log Analysis
       |
       v
Threat Detection
       |
       v
Evidence Correlation
       |
       v
IOC Extraction
       |
       v
Incident Investigation
       |
       v
Documentation
```

---

## Design Goals

The architecture was designed around the following principles:

- Multiple sources of security telemetry
- Network and endpoint visibility
- Controlled attack simulation
- Evidence-based investigation
- IOC identification
- Practical SOC workflow experience
- Correlation of network and endpoint evidence

---

## Lab Scope

This was a controlled home lab created for cybersecurity learning and defensive security practice.

The environment was intended to simulate selected aspects of a SOC monitoring and investigation workflow without representing a production enterprise environment.
