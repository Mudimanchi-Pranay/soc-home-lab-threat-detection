# CrowdSec – Threat Detection Component

## Overview

CrowdSec was used as part of the SOC home lab's defensive security and threat detection environment.

It provided an additional layer of visibility for identifying and responding to suspicious activity within the controlled lab environment.

---

## Role in the SOC Lab

CrowdSec supported the defensive monitoring workflow of the lab.

Its role included:

- Threat detection
- Identification of suspicious activity
- Defensive security monitoring
- Supporting investigation of security events
- Providing additional context during incident analysis

---

## Position in the Architecture

```text
                    Security Activity
                           |
                           v
                    +-------------+
                    |   CrowdSec  |
                    |    Threat   |
                    |  Detection  |
                    +------+------+
                           |
                           v
                    Security Evidence
                           |
                           v
                     Investigation
```

---

## Threat Detection Workflow

The general workflow involving CrowdSec can be represented as:

```text
Security Activity
       |
       v
Threat Detection
       |
       v
Suspicious Activity
       |
       v
Security Evidence
       |
       v
Log Analysis
       |
       v
IOC Identification
       |
       v
Incident Investigation
```

---

## Integration with the SOC Lab

CrowdSec was considered alongside the other security components in the lab.

### pfSense

Provided network-level visibility and firewall-related security information.

### Sysmon

Provided endpoint telemetry for investigating activity occurring on monitored systems.

### CrowdSec

Provided an additional defensive threat detection capability.

Together, these components provided complementary visibility across network and endpoint security activity.

---

## Investigation Context

Threat detection information can help an analyst understand:

- Whether suspicious activity was observed
- What activity requires further investigation
- Whether additional evidence should be collected
- How detected activity relates to other network or endpoint observations

CrowdSec-related observations could therefore be considered together with available network and endpoint evidence.

---

## Detection and Investigation Flow

```text
             +----------------+
             |    pfSense     |
             | Network Data   |
             +-------+--------+
                     |
                     |
                     v
              +-------------+
              | Correlation |
              +------+------+
                     ^
                     |
                     |
             +-------+--------+
             |    Sysmon      |
             | Endpoint Data  |
             +----------------+

                     |
                     v

             +-------------+
             |   CrowdSec  |
             |   Threat    |
             |  Detection  |
             +------+------+
                    |
                    v
             Suspicious Activity
                    |
                    v
               Investigation
                    |
                    v
               IOC Analysis
```

---

## SOC Analyst Perspective

From a SOC analyst perspective, a dedicated threat detection component can provide an additional signal when analyzing suspicious activity.

Combining detection information with network and endpoint telemetry can help improve:

- Alert investigation
- Evidence correlation
- Threat identification
- Incident scoping
- IOC analysis

---

## Key Learning Outcomes

Working with CrowdSec in the lab helped develop practical understanding of:

- Defensive threat detection
- Security monitoring
- Suspicious activity analysis
- Security event investigation
- Correlation of multiple security data sources
- IOC identification
- SOC investigation workflows

---

## Lab Scope

CrowdSec was used within a controlled cybersecurity home lab for defensive security learning, threat detection practice, and incident investigation exercises.
