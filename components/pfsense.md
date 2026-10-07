# pfSense – Network Security Component

## Overview

pfSense was used as the firewall and network security component of the SOC home lab.

It provided network-level visibility that could be used alongside endpoint telemetry during security monitoring, threat detection, and incident investigation.

---

## Role in the SOC Lab

The primary role of pfSense was to provide network-level security visibility within the controlled lab environment.

It supported:

- Network security monitoring
- Firewall-based traffic visibility
- Analysis of network activity generated during security simulations
- Investigation of suspicious network behavior
- Correlation with endpoint telemetry

---

## Position in the Architecture

```text
                    Attack Simulation
                           |
                           v
                    Network Activity
                           |
                           v
                    +-------------+
                    |   pfSense   |
                    |   Firewall  |
                    +------+------+
                           |
              +------------+------------+
              |                         |
              v                         v
       Network Telemetry        Endpoint Activity
                                        |
                                        v
                                     Sysmon
```

---

## Network Monitoring

pfSense formed the network visibility layer of the SOC home lab.

Network activity generated during security exercises could be examined through the firewall layer and considered as part of the overall investigation.

This provided network-level context that could be correlated with endpoint activity.

---

## Security Monitoring Workflow

The general network monitoring workflow was:

```text
Network Activity
       |
       v
     pfSense
       |
       v
Network-Level Evidence
       |
       v
   Log Analysis
       |
       v
Suspicious Activity
       |
       v
Correlation with
Endpoint Telemetry
       |
       v
Incident Investigation
```

---

## Investigation Use

Network-level information can provide useful context during a security investigation, including:

- Source and destination communication
- Observed network activity
- Suspicious connection behavior
- Firewall-related security events
- Network activity associated with simulated security events

This information can then be considered together with endpoint telemetry to improve investigation context.

---

## Correlation with Endpoint Telemetry

pfSense network visibility was considered alongside Sysmon endpoint telemetry.

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

Combining network and endpoint evidence can help an analyst develop a more complete understanding of suspicious activity.

---

## Integration with Other Components

### Sysmon

Sysmon provided endpoint-level telemetry for investigating activity occurring on monitored systems.

### CrowdSec

CrowdSec provided an additional defensive threat detection capability within the lab.

Together, these components provided complementary visibility across network and endpoint activity.

---

## SOC Analyst Perspective

From a SOC analyst perspective, firewall telemetry can help answer questions such as:

- Where did the activity originate?
- Which systems were involved?
- What network activity was observed?
- What connections were associated with the event?
- Does the network evidence support the endpoint observations?
- Does the activity require further investigation?

---

## Key Learning Outcomes

Working with pfSense in the lab helped develop practical understanding of:

- Firewall-based security monitoring
- Network visibility
- Network evidence analysis
- Security event investigation
- Network and endpoint correlation
- Threat detection workflows
- Incident investigation

---

## Lab Scope

pfSense was used within a controlled cybersecurity home lab for defensive security learning, threat detection practice, network monitoring, and incident investigation exercises.
