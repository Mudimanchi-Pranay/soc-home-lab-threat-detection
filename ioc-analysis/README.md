# IOC Analysis

## Overview

Indicator of Compromise (IOC) analysis was practiced as part of the SOC home lab investigation workflow.

The purpose of IOC analysis was to identify security-relevant indicators from available network and endpoint evidence and use them to support incident investigation.

---

## What is an IOC?

An Indicator of Compromise is an observable artifact that may provide evidence of potentially malicious or suspicious activity.

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

## IOC Sources

Potential indicators can be identified from multiple sources within the lab.

### Network Evidence

Network-level evidence can provide indicators such as:

- Source IP addresses
- Destination IP addresses
- Domains
- URLs
- Suspicious network connections

### Endpoint Evidence

Endpoint telemetry can provide indicators such as:

- Suspicious processes
- File names
- File hashes
- Unusual activity
- Other host-level artifacts

### Threat Detection Evidence

Threat detection information can provide additional indicators that may require investigation and validation.

---

## IOC Validation

Not every suspicious artifact should automatically be treated as a confirmed IOC.

A potential indicator should be evaluated using the available evidence.

The investigation should consider:

1. Where the indicator was observed
2. When it was observed
3. What activity was associated with it
4. Whether other telemetry supports the finding
5. Whether the indicator is relevant to the investigation

---

## IOC Documentation

A structured IOC record can be maintained using the following format:

| IOC Type | Indicator | Source | Context | Status |
|---|---|---|---|---|
| IP Address | `<indicator>` | Network telemetry | Suspicious communication | To be validated |
| Domain | `<indicator>` | Network telemetry | Suspicious activity | To be validated |
| File Hash | `<indicator>` | Endpoint telemetry | Suspicious file | To be validated |
| Process | `<indicator>` | Endpoint telemetry | Suspicious activity | To be validated |

> Placeholder values are intentionally used because this repository documents the lab methodology rather than inventing historical IOC values that are no longer available.

---

## IOC Correlation

IOC analysis becomes more useful when indicators are correlated with other evidence.

```text
              Network Evidence
                     |
                     v
               IP / Domain
                     |
                     |
                     v
                 Correlation
                     ^
                     |
                     |
              Endpoint Evidence
                     |
                     v
            Process / File Hash
                     |
                     v
              IOC Analysis
                     |
                     v
            Incident Investigation
```

---

## Investigation Use

Identified and validated IOCs can support:

- Incident scoping
- Evidence correlation
- Threat investigation
- Detection improvement
- Future security monitoring
- Incident documentation

---

## SOC Analyst Perspective

IOC analysis is an important part of incident investigation because indicators can help connect seemingly separate security events.

A SOC analyst should avoid treating every artifact as malicious without supporting evidence.

The goal is to distinguish between:

**Observed Artifact → Potential IOC → Validated IOC**

based on the available evidence.

---

## Key Learning Outcomes

This lab provided practical exposure to:

- IOC identification
- IOC categorization
- Network indicator analysis
- Endpoint indicator analysis
- Evidence validation
- IOC correlation
- Incident investigation
- Security documentation

---

## Lab Scope

IOC analysis was practiced within a controlled cybersecurity home lab for defensive security learning and SOC analyst skill development.
