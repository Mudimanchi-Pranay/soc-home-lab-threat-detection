# pfSense – Network Security Component

## Overview

pfSense was used as the firewall and network security component of the SOC home lab.

It provided network-level visibility that could be used alongside endpoint telemetry during security monitoring and incident investigation.

---

## Role in the SOC Lab

The primary role of pfSense was to provide visibility into network activity within the controlled lab environment.

This supported:

- Network security monitoring
- Firewall-based traffic visibility
- Analysis of network activity generated during attack simulations
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
             +-------------+-------------+
             |                           |
             v                           v
      Network Telemetry          Endpoint Activity
                                         |
                                         v
                                      Sysmon
