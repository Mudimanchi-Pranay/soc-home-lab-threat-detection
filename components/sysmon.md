# Sysmon – Endpoint Telemetry Component

## Overview

Sysmon (System Monitor) was used in the SOC home lab to provide endpoint telemetry for security monitoring and investigation.

The endpoint telemetry provided additional visibility into activity occurring on monitored systems during security exercises.

---

## Role in the SOC Lab

Sysmon formed the endpoint visibility layer of the lab.

It supported:

- Endpoint activity monitoring
- Security event analysis
- Investigation of suspicious activity
- Identification of potentially relevant processes and activities
- Correlation with network-level evidence

---

## Position in the Architecture

```text
                    Network Activity
                           |
                           v
                       pfSense
                           |
                           v
                   Endpoint Activity
                           |
                           v
                    +-------------+
                    |    Sysmon   |
                    |  Telemetry  |
                    +------+------+
                           |
                           v
                    Endpoint Logs
                           |
                           v
                    Investigation
```

---

## Endpoint Telemetry

Sysmon provides detailed information about activity occurring on a Windows endpoint.

Within the lab, endpoint telemetry was used as an additional source of evidence during security investigations.

This helped provide context around activity observed during simulated security events.

---

## Investigation Workflow

The endpoint investigation workflow can be represented as:

```text
Endpoint Activity
       |
       v
Sysmon Telemetry
       |
       v
Security Events
       |
       v
Log Analysis
       |
       v
Suspicious Activity
       |
       v
IOC Identification
       |
       v
Incident Investigation
```

---

## Endpoint and Network Correlation

One of the objectives of the lab was to understand the value of combining endpoint and network visibility.

```text
             Network Evidence
                    |
                    v
                 pfSense
                    |
                    v
              Network Context
                    |
                    +---------+
                              |
                              v
                         Correlation
                              ^
                              |
                    +---------+
                    |
                 Sysmon
                    |
                    v
             Endpoint Evidence
```

Network-level observations could be compared with endpoint telemetry to develop a better understanding of suspicious activity.

---

## Investigation Value

Endpoint telemetry can help answer questions such as:

- What activity occurred on the endpoint?
- Which processes or activities were associated with the event?
- When did the activity occur?
- Does endpoint evidence support the network observations?
- Are there indicators that require further investigation?

---

## SOC Analyst Perspective

From a SOC analyst perspective, endpoint telemetry is important because network activity alone may not provide enough context to understand what happened on a system.

Combining endpoint evidence with network evidence can improve:

- Detection accuracy
- Investigation context
- Incident scoping
- IOC identification
- Threat analysis

---

## Key Learning Outcomes

Working with Sysmon in the lab helped develop practical understanding of:

- Endpoint telemetry
- Security event analysis
- Host-based investigation
- Evidence correlation
- IOC identification
- Incident investigation workflows

---

## Lab Scope

Sysmon was used as part of a controlled cybersecurity home lab for defensive security learning, threat detection practice, and SOC investigation exercises.
