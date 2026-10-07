# SOC Home Lab – Threat Detection Environment

A hands-on Security Operations Center (SOC) home lab designed to practice **security monitoring, threat detection, log analysis, endpoint telemetry, network visibility, IOC extraction, and incident investigation**.

The environment integrated **pfSense, Sysmon, and CrowdSec** to provide complementary network and endpoint security visibility within a controlled cybersecurity lab.

---

## Table of Contents

- [Overview](#overview)
- [Objectives](#objectives)
- [Lab Architecture](#lab-architecture)
- [Core Components](#core-components)
  - [pfSense](#pfsense)
  - [Sysmon](#sysmon)
  - [CrowdSec](#crowdsec)
- [Telemetry Sources](#telemetry-sources)
- [Attack Simulations](#attack-simulations)
- [Detection Workflow](#detection-workflow)
- [Incident Investigation](#incident-investigation)
- [IOC Analysis](#ioc-analysis)
- [Evidence Correlation](#evidence-correlation)
- [SOC Analyst Perspective](#soc-analyst-perspective)
- [Investigation Documentation](#investigation-documentation)
- [Screenshots and Visual Documentation](#screenshots-and-visual-documentation)
- [Key Learning Outcomes](#key-learning-outcomes)
- [Future Improvements](#future-improvements)
- [Repository Structure](#repository-structure)
- [Lab Scope](#lab-scope)

---

# Overview

The SOC Home Lab was designed as a controlled environment for practicing the workflow followed by security analysts when detecting and investigating suspicious activity.

The lab combined:

- Network security monitoring
- Firewall-based visibility
- Endpoint telemetry
- Threat detection
- Security log analysis
- Attack simulation
- Evidence correlation
- IOC identification
- Incident investigation
- Security documentation

The overall objective was to understand how different security technologies can work together to provide visibility across network and endpoint activity.

---

# Objectives

The main objectives of the lab were to:

- Build a practical SOC monitoring environment
- Understand network-level security visibility
- Understand endpoint telemetry
- Generate controlled security activity
- Analyze security-relevant logs
- Identify suspicious behavior
- Correlate network and endpoint evidence
- Extract potential indicators of compromise
- Practice incident investigation
- Develop a defensive SOC analyst mindset
- Document security findings and investigation workflows

---

# Lab Architecture

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

# Core Components

## pfSense

pfSense was used as the firewall and network security component of the SOC home lab.

It provided network-level visibility that could be considered alongside endpoint telemetry during security monitoring, threat detection, and incident investigation.

### Role

pfSense supported:

- Network security monitoring
- Firewall-based traffic visibility
- Analysis of network activity
- Investigation of suspicious network behavior
- Correlation with endpoint telemetry

### Network Monitoring

Network activity generated during security exercises could be observed through the firewall layer.

The network evidence provided additional context during investigations.

### Investigation Questions

Network analysis can help answer questions such as:

- What network activity was generated?
- Which systems were involved?
- What communication was observed?
- Was the activity suspicious?
- What network evidence supports the investigation?

---

## Sysmon

Sysmon (System Monitor) was used to provide endpoint telemetry within the SOC home lab.

The telemetry provided additional visibility into activity occurring on monitored systems during security exercises.

### Role

Sysmon supported:

- Endpoint activity monitoring
- Security event analysis
- Investigation of suspicious activity
- Identification of relevant processes and activities
- Correlation with network-level evidence

### Endpoint Telemetry

Sysmon provided endpoint-level evidence that could be used as part of security investigations.

This helped provide context around activity observed during simulated security events.

### Investigation Questions

Endpoint analysis can help answer:

- What activity occurred on the endpoint?
- What processes or activities were associated with the event?
- When did the activity occur?
- Was there evidence requiring further investigation?
- Could endpoint evidence be correlated with network activity?

---

## CrowdSec

CrowdSec was incorporated as part of the defensive threat detection environment.

It provided an additional security layer for identifying and analyzing suspicious activity within the controlled lab.

### Role

CrowdSec supported:

- Threat detection
- Identification of suspicious activity
- Defensive security monitoring
- Security event investigation
- Additional context during incident analysis

### Investigation Context

Threat detection information can help an analyst determine:

- Whether suspicious activity was observed
- What activity requires further investigation
- Whether additional evidence should be collected
- How detected activity relates to network and endpoint observations

---

# Telemetry Sources

The lab considered two primary visibility layers.

## Network Telemetry

Network-level activity was observed through the firewall and network security layer.

Network telemetry can provide information about:

- Source systems
- Destination systems
- Network communication
- Suspicious connections
- Firewall-related activity
- Network behavior

## Endpoint Telemetry

Endpoint activity was monitored using Sysmon-generated telemetry.

Endpoint telemetry can provide information about:

- Endpoint activity
- Processes
- Security events
- Suspicious behavior
- Host-level evidence

These different sources provide complementary evidence during investigations.

---

# Attack Simulations

The SOC home lab included controlled attack simulations to generate security-relevant activity for detection, monitoring, and investigation practice.

The objective was not simply to generate an attack, but to understand how suspicious activity appears across network and endpoint telemetry.

## Simulation Objectives

The simulations were designed to:

- Generate controlled security activity
- Observe network-level activity
- Observe endpoint-level activity
- Analyze resulting logs
- Identify suspicious behavior
- Extract relevant indicators
- Practice incident investigation
- Understand attack activity from a defensive perspective

## Simulation Workflow

```text
Controlled Attack Simulation
            |
            v
     Security Activity
            |
       +----+----+
       |         |
       v         v
    Network   Endpoint
    Activity  Activity
       |         |
       v         v
    pfSense    Sysmon
       |         |
       +----+----+
            |
            v
       Log Analysis
            |
            v
     Threat Detection
            |
            v
      IOC Extraction
            |
            v
  Incident Investigation
```

---

# Detection Workflow

The detection workflow focused on identifying suspicious activity using network and endpoint telemetry.

## Detection Lifecycle

```text
Security Activity
       |
       v
Telemetry Generated
       |
       v
Log Collection
       |
       v
Log Analysis
       |
       v
Suspicious Activity Identified
       |
       v
Evidence Correlation
       |
       v
IOC Identification
       |
       v
Incident Investigation
```

## Detection Sources

### pfSense

Provided network-level security visibility.

### Sysmon

Provided endpoint telemetry.

### CrowdSec

Provided an additional defensive threat detection capability.

---

## Network Detection

Network activity was reviewed to identify potentially suspicious communication and security-relevant events.

Analysis considered:

- Network activity
- Source and destination systems
- Communication patterns
- Suspicious connections
- Firewall-related information
- Relationship to simulated security activity

---

## Endpoint Detection

Sysmon telemetry provided additional information about activity occurring on monitored systems.

Analysis considered:

- Endpoint activity
- Processes or activities associated with events
- Timing of activity
- Suspicious behavior
- Relationship to network activity

---

# Incident Investigation

The lab practiced a structured approach to investigating suspicious security activity.

The investigation combined network and endpoint evidence to understand the activity, identify relevant indicators, and document findings.

## Investigation Lifecycle

```text
Suspicious Activity
        |
        v
   Initial Triage
        |
        v
   Evidence Collection
        |
        v
     Log Analysis
        |
        v
Network + Endpoint
    Correlation
        |
        v
    IOC Extraction
        |
        v
   Incident Scoping
        |
        v
 Findings & Analysis
        |
        v
   Documentation
```

---

## Initial Triage

The first stage was to understand the available security information and determine whether the observed activity required further investigation.

Questions included:

- What activity was observed?
- When did it occur?
- Which systems were involved?
- What type of activity was observed?
- Is the activity potentially suspicious?

---

## Evidence Collection

Relevant evidence could be collected from:

- pfSense network information
- Sysmon endpoint telemetry
- CrowdSec threat detection information
- Other available security logs

---

## Log Analysis

Collected logs were reviewed to understand the sequence of activity.

Analysis focused on:

- Event timing
- Source and destination information
- Endpoint activity
- Network activity
- Suspicious behavior
- Relationships between events

---

## Incident Scoping

The potential scope of the activity was assessed by considering:

- Systems involved
- Activity observed
- Related events
- Available indicators
- Potentially affected systems

---

# Evidence Correlation

A major objective of the lab was understanding how multiple telemetry sources can be combined.

```text
             Network Evidence
                    |
                    v
                 pfSense
                    |
                    v
              Network Context
                    |
                    |
                    v
                Correlation
                    ^
                    |
                    |
              Endpoint Context
                    ^
                    |
                 Sysmon
                    |
                    v
             Endpoint Evidence
```

Correlation helps determine whether network observations are consistent with activity observed on an endpoint.

---

# IOC Analysis

Indicator of Compromise (IOC) analysis was practiced as part of the investigation workflow.

## What is an IOC?

An IOC is an observable artifact that may provide evidence of potentially malicious or suspicious activity.

Common IOC categories include:

- IP addresses
- Domains
- URLs
- File hashes
- File names
- Suspicious processes
- Network indicators
- Other security-relevant artifacts

---

## IOC Analysis Workflow

```text
Security Event
      |
      v
Evidence Collection
      |
      v
Log Analysis
      |
      v
Identify Relevant Artifacts
      |
      v
Extract Potential IOCs
      |
      v
Validate Evidence
      |
      v
Document IOCs
      |
      v
Use IOCs for Investigation
```

---

## IOC Validation

Not every suspicious artifact should automatically be treated as a confirmed IOC.

The investigation should consider:

1. Where the indicator was observed
2. When it was observed
3. What activity was associated with it
4. Whether other telemetry supports the finding
5. Whether the indicator is relevant to the investigation

The workflow therefore distinguishes between:

```text
Observed Artifact
       |
       v
Potential IOC
       |
       v
Validated IOC
```

---

# Investigation Documentation

A structured investigation record can include:

| Field | Description |
|---|---|
| Incident | Short description of the activity |
| Date/Time | Time associated with the observed activity |
| Systems | Systems involved |
| Evidence | Relevant network and endpoint evidence |
| IOCs | Identified indicators |
| Analysis | Investigation findings |
| Scope | Potential impact or affected systems |
| Conclusion | Final assessment based on available evidence |

The investigation should distinguish between **observed evidence**, **analysis**, and **potential indicators** to avoid unsupported conclusions.

---

# SOC Analyst Perspective

The lab was designed around a practical SOC workflow:

```text
Detect
  |
  v
Triage
  |
  v
Collect Evidence
  |
  v
Analyze
  |
  v
Correlate
  |
  v
Extract IOCs
  |
  v
Investigate
  |
  v
Document
```

A SOC analyst should not rely on a single event or telemetry source when investigating suspicious activity.

The objective is to move from:

**Detection → Evidence → Correlation → Analysis → Investigation → Documentation**

---

# Screenshots and Visual Documentation

The `screenshots/` directory contains visual references for the major components of the lab.

The repository includes visual references for:

1. Lab architecture
2. pfSense dashboard
3. pfSense firewall logs
4. Sysmon installation
5. Sysmon event logs
6. Sysmon process creation telemetry
7. CrowdSec overview
8. CrowdSec alerts
9. CrowdSec scenario status

> **Important:** The original lab environment is no longer available locally. Therefore, the visual references in this repository are clearly identified as illustrative representations and are not claimed to be historical screenshots from the original environment.

The detailed visual documentation is available in [`screenshots/README.md`](./screenshots/README.md).

---

# Key Learning Outcomes

The lab provided practical exposure to:

- Security monitoring
- Network security monitoring
- Endpoint telemetry
- Threat detection
- Firewall-based visibility
- Security event analysis
- Log investigation
- Evidence correlation
- IOC identification
- Incident scoping
- Incident investigation
- Security documentation
- Defensive security workflows

---

# Major Lessons Learned

## Multiple Telemetry Sources Matter

Network and endpoint telemetry provide different perspectives of the same activity.

```text
Network Visibility
       +
Endpoint Visibility
       |
       v
Better Investigation Context
```

---

## Detection Is Only the Beginning

Identifying suspicious activity is only the first stage.

A complete SOC workflow requires investigation, evidence collection, correlation, IOC analysis, and documentation.

---

## Evidence-Based Investigation

Security investigations should be based on available evidence rather than assumptions.

```text
Observed Evidence
       |
       v
Analysis
       |
       v
Correlation
       |
       v
Conclusion
```

---

## Defensive Security Mindset

The lab focused on understanding:

- How suspicious activity appears in telemetry
- How activity can be detected
- What evidence it generates
- How an analyst can investigate it
- Which indicators can support the investigation
- How findings should be documented

---

# Future Improvements

If the lab is rebuilt in the future, possible improvements include:

- Centralized log collection
- SIEM integration
- Additional endpoint telemetry
- Additional detection use cases
- Automated alerting
- Structured incident response playbooks
- Additional attack simulations
- Detection rule development
- Automated IOC enrichment
- Improved dashboards and visualization

---

# Repository Structure

```text
soc-home-lab-threat-detection/
│
├── README.md
├── LICENSE
├── .gitignore
│
├── architecture/
│   └── architecture.md
│
├── components/
│   ├── README.md
│   ├── pfsense.md
│   ├── sysmon.md
│   └── crowdsec.md
│
├── attack-simulations/
│   └── README.md
│
├── detection/
│   └── detection-workflow.md
│
├── investigation/
│   └── investigation-workflow.md
│
├── ioc-analysis/
│   └── README.md
│
├── screenshots/
│   ├── README.md
│   ├── architecture-lab-topology.png
│   ├── pfsense-dashboard.png
│   ├── pfsense-firewall-logs.png
│   ├── sysmon-installation.png
│   ├── sysmon-event-logs.png
│   ├── sysmon-process-create.png
│   ├── crowdsec-metrics.png
│   ├── crowdsec-alerts.png
│   └── crowdsec-scenarios.png
│
└── docs/
    └── lessons-learned.md
```

---

# Technologies

| Technology | Purpose |
|---|---|
| pfSense | Firewall and network security visibility |
| Sysmon | Endpoint telemetry |
| CrowdSec | Defensive threat detection |
| Windows | Endpoint monitoring environment |
| Linux | Security tooling environment |
| SOC Methodology | Detection and investigation workflow |

---

# Lab Scope

This project was developed as a **controlled cybersecurity home lab** for defensive security learning and SOC analyst skill development.

The environment was designed to simulate selected aspects of a SOC monitoring and investigation workflow rather than represent a production enterprise environment.

All security exercises were intended for controlled lab environments.

---

# Final Project Summary

The SOC Home Lab brought together:

```text
             Attack Simulation
                    |
                    v
              Security Activity
                    |
          +---------+---------+
          |                   |
          v                   v
       Network             Endpoint
       Activity             Activity
          |                   |
          v                   v
       pfSense              Sysmon
          |                   |
          +---------+---------+
                    |
                    v
               Correlation
                    |
                    v
             Threat Detection
                    |
                    v
              IOC Analysis
                    |
                    v
          Incident Investigation
                    |
                    v
              Documentation
```

The project provided practical experience in connecting security technologies with a complete defensive SOC workflow:

**Monitor → Detect → Investigate → Correlate → Extract IOCs → Document**

---

## Related Documentation

Detailed documentation is available throughout the repository:

- [Architecture](./architecture/architecture.md)
- [Components](./components/README.md)
- [Attack Simulations](./attack-simulations/README.md)
- [Detection Workflow](./detection/detection-workflow.md)
- [Investigation Workflow](./investigation/investigation-workflow.md)
- [IOC Analysis](./ioc-analysis/README.md)
- [Screenshots & Visual Documentation](./screenshots/README.md)
- [Lessons Learned](./docs/lessons-learned.md)
