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
                    |  IOC Extraction      |
                    +----------+-----------+
                               |
                               v
                    +----------------------+
                    | Incident Investigation|
                    +----------------------+
