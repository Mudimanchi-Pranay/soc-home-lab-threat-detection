# Detection Workflow

## Overview

The SOC home lab was designed to practice the process of identifying suspicious activity using network and endpoint telemetry.

The detection workflow focused on observing security activity, reviewing available evidence, identifying suspicious behavior, and preparing the activity for further investigation.

---

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

---

## Detection Sources

The lab used multiple sources of security visibility.

### pfSense

Provided network-level visibility and firewall-related security information.

### Sysmon

Provided endpoint telemetry for analyzing activity occurring on monitored systems.

### CrowdSec

Provided an additional defensive threat detection capability.

---

## Network Detection

Network activity was reviewed to identify potentially suspicious communication and security-relevant events.

The analysis considered:

- Network activity
- Source and destination systems
- Communication patterns
- Suspicious connections
- Firewall-related information
- Relationship to simulated security activity

Network evidence could then be correlated with endpoint information.

---

## Endpoint Detection

Endpoint telemetry from Sysmon provided additional information about activity occurring on monitored systems.

The analysis considered:

- Endpoint activity
- Processes or activities associated with an event
- Timing of activity
- Suspicious behavior
- Relationship to network activity

---

## Threat Detection Correlation

A major objective of the lab was to understand how multiple telemetry sources can be combined during detection.

```text
              Network Evidence
                     |
                     v
                  pfSense
                     |
                     |
                     v
                +---------+
                |         |
                |Correlation
                |         |
                +---------+
                     ^
                     |
                     |
                  Sysmon
                     |
                     v
              Endpoint Evidence
                     |
                     v
              Detection Context
```

Combining network and endpoint evidence can provide stronger context than relying on a single source of telemetry.

---

## Detection Analysis

When suspicious activity was identified, the investigation considered:

1. What activity occurred?
2. When did it occur?
3. Which systems were involved?
4. What network evidence was available?
5. What endpoint evidence was available?
6. Could the evidence be correlated?
7. Were there identifiable indicators of compromise?
8. Did the activity require further investigation?

---

## IOC Identification

Relevant indicators could be extracted from the available security evidence.

Potential IOC categories include:

- IP addresses
- Domains
- File hashes
- Suspicious processes
- Network indicators
- Other relevant security indicators

Indicators should only be documented as confirmed when supported by available evidence.

---

## Detection-to-Investigation Flow

```text
                Detection
                   |
                   v
            Suspicious Activity
                   |
                   v
             Evidence Review
                   |
                   v
          Network + Endpoint
             Correlation
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

## SOC Analyst Perspective

The detection workflow demonstrates the importance of moving beyond simply identifying an alert.

A SOC analyst should be able to:

- Understand the observed activity
- Review supporting evidence
- Correlate multiple telemetry sources
- Identify relevant indicators
- Determine whether additional investigation is required
- Document the findings

---

## Key Learning Outcomes

This workflow provided practical experience with:

- Security monitoring
- Threat detection
- Network telemetry analysis
- Endpoint telemetry analysis
- Evidence correlation
- IOC identification
- Incident investigation
- SOC investigation methodology

---

## Lab Scope

The detection workflow was practiced within a controlled cybersecurity home lab for defensive security learning and SOC analyst skill development.
