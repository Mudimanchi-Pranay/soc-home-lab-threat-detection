# Attack Simulations

## Overview

The SOC home lab included controlled attack simulations to generate security-relevant activity for detection, monitoring, and investigation practice.

The purpose of the simulations was to understand how suspicious activity can appear across network and endpoint telemetry and how a SOC analyst can investigate the resulting evidence.

---

## Objectives

The attack simulation exercises were designed to:

- Generate controlled security activity
- Observe network-level activity
- Observe endpoint-level activity
- Analyze resulting security logs
- Identify suspicious behavior
- Extract relevant indicators
- Practice incident investigation
- Understand the relationship between attack activity and security telemetry

---

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

## Network-Level Activity

Network activity generated during simulations could be observed through the network security layer.

The purpose was to understand how simulated security activity could be reflected in network telemetry and how this evidence could support investigation.

### Investigation Focus

Network analysis focused on questions such as:

- What network activity was generated?
- Which systems were involved?
- What communication was observed?
- Was the activity suspicious?
- What network evidence could support the investigation?

---

## Endpoint-Level Activity

Endpoint activity generated during simulations could be observed through Sysmon telemetry.

The endpoint evidence provided additional context for understanding activity occurring on monitored systems.

### Investigation Focus

Endpoint analysis focused on questions such as:

- What activity occurred on the endpoint?
- What processes or activities were associated with the event?
- When did the activity occur?
- Was there evidence requiring further investigation?
- Could endpoint evidence be correlated with network activity?

---

## Evidence Collection

The simulations provided multiple sources of evidence.

```text
                 Attack Simulation
                        |
          +-------------+-------------+
          |                           |
          v                           v
    Network Evidence           Endpoint Evidence
          |                           |
          v                           v
       pfSense                      Sysmon
          |                           |
          +-------------+-------------+
                        |
                        v
                 Evidence Correlation
                        |
                        v
                  Investigation
```

---

## Detection Workflow

The generated activity was analyzed using a basic SOC detection workflow:

```text
Activity Generated
        |
        v
Telemetry Observed
        |
        v
Logs Reviewed
        |
        v
Suspicious Activity Identified
        |
        v
Evidence Correlated
        |
        v
IOCs Extracted
        |
        v
Incident Investigated
```

---

## IOC Identification

During investigation, relevant indicators could be identified from available security telemetry.

Potential IOC categories include:

- IP addresses
- Domains
- File hashes
- Suspicious processes
- Network indicators
- Other relevant security indicators

Only indicators supported by available evidence should be documented as confirmed IOCs.

---

## Investigation Approach

The attack simulations were treated as controlled security exercises rather than isolated attack demonstrations.

The investigation approach focused on:

1. Understanding the generated activity
2. Reviewing available telemetry
3. Identifying suspicious behavior
4. Correlating network and endpoint evidence
5. Extracting relevant indicators
6. Determining the potential scope of the activity
7. Documenting the investigation

---

## SOC Analyst Perspective

Attack simulation is useful in a SOC lab because it allows an analyst to practice the complete detection and investigation lifecycle in a controlled environment.

The objective is not only to generate an attack, but to understand:

**What happened → What evidence was generated → How it was detected → How it was investigated → What indicators were identified**

---

## Lab Scope

All attack simulations were performed within a controlled cybersecurity home lab for defensive learning and SOC analyst skill development.

This repository does not provide instructions for targeting unauthorized systems.
