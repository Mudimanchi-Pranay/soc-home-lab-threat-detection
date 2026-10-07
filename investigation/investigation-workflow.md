# Incident Investigation Workflow

## Overview

The SOC home lab was used to practice a structured approach to investigating suspicious security activity.

The investigation process combined network and endpoint evidence to understand the activity, identify relevant indicators, and document the findings.

---

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

## Step 1 – Initial Triage

The first stage of an investigation is to understand the available security information and determine whether the observed activity requires further analysis.

Initial triage considers:

- What activity was observed?
- When did it occur?
- Which system or systems were involved?
- What type of activity was observed?
- Is the activity potentially suspicious?

---

## Step 2 – Evidence Collection

Relevant security evidence can be collected from the available telemetry sources within the lab.

Primary sources included:

- pfSense network information
- Sysmon endpoint telemetry
- CrowdSec threat detection information
- Other available security logs

The purpose of evidence collection is to establish sufficient context for further investigation.

---

## Step 3 – Log Analysis

Collected logs are reviewed to understand the sequence of activity.

The analysis focuses on:

- Event timing
- Source and destination information
- Endpoint activity
- Network activity
- Suspicious behavior
- Relationships between different events

---

## Step 4 – Network and Endpoint Correlation

Network and endpoint evidence can provide different perspectives of the same activity.

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

Correlation helps determine whether network observations are consistent with activity observed on the endpoint.

---

## Step 5 – IOC Extraction

Relevant indicators are identified from the available evidence.

Potential IOC categories include:

- IP addresses
- Domains
- File hashes
- Suspicious processes
- Network indicators
- Other relevant indicators

Only indicators supported by the available evidence should be treated as confirmed findings.

---

## Step 6 – Incident Scoping

After analyzing the evidence, the potential scope of the activity can be assessed.

Questions include:

- Which systems were involved?
- What activity was observed?
- How much evidence is available?
- Are there related events?
- Are additional systems potentially affected?
- Are additional indicators present?

---

## Step 7 – Findings and Analysis

The evidence is analyzed to develop an understanding of what occurred.

A structured investigation should distinguish between:

### Observed Evidence

Information directly supported by available telemetry.

### Analysis

Interpretation of the observed evidence.

### Potential Indicators

Items that may require additional validation before being treated as confirmed IOCs.

This approach helps avoid making unsupported conclusions during an investigation.

---

## Step 8 – Documentation

Investigation findings should be documented in a structured manner.

A basic investigation record can include:

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

---

## Investigation Workflow Summary

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
Analyze Logs
  |
  v
Correlate Evidence
  |
  v
Extract IOCs
  |
  v
Scope Activity
  |
  v
Analyze Findings
  |
  v
Document Investigation
```

---

## SOC Analyst Perspective

A SOC analyst should not rely on a single event when investigating suspicious activity.

A structured investigation combines:

**Detection + Evidence + Correlation + Analysis + Documentation**

The objective is to move from an initial suspicious event toward a defensible understanding of what occurred.

---

## Key Learning Outcomes

This investigation workflow provided practical experience with:

- Security alert triage
- Evidence collection
- Log analysis
- Network investigation
- Endpoint investigation
- Evidence correlation
- IOC extraction
- Incident scoping
- Investigation documentation

---

## Lab Scope

This investigation methodology was practiced within a controlled cybersecurity home lab for defensive security learning and SOC analyst skill development.
