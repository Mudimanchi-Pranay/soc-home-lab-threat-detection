# Lessons Learned

## Overview

Building and working with the SOC home lab provided practical experience with defensive cybersecurity concepts and SOC investigation workflows.

The lab focused on understanding how network and endpoint security information can be combined to investigate suspicious activity.

---

## 1. Importance of Multiple Telemetry Sources

One of the major lessons from the lab was the importance of having visibility from more than one source.

Network telemetry and endpoint telemetry provide different perspectives of the same activity.

```text
Network Visibility
       +
Endpoint Visibility
       |
       v
Better Investigation Context
```

A single source of information may not provide enough context to understand an incident.

---

## 2. Network Visibility

Working with pfSense provided practical exposure to network-level security monitoring.

Network evidence can help an analyst understand:

- Communication between systems
- Suspicious network activity
- Source and destination information
- Network behavior associated with security events

---

## 3. Endpoint Visibility

Sysmon provided endpoint-level telemetry that can complement network evidence.

Endpoint visibility can help answer questions about activity occurring directly on a monitored system.

This demonstrated why endpoint telemetry is valuable during incident investigations.

---

## 4. Importance of Correlation

A major learning from the lab was that security events should not always be analyzed in isolation.

Correlating network and endpoint evidence can provide stronger investigation context.

```text
Network Evidence
       |
       +---------+
                 |
                 v
             Correlation
                 ^
       +---------+
       |
Endpoint Evidence
       |
       v
Investigation Context
```

---

## 5. Detection Is Only the Beginning

Identifying suspicious activity is only the first stage of a SOC workflow.

A complete workflow involves:

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

This helped reinforce the importance of investigation after an alert or suspicious event is identified.

---

## 6. IOC Analysis

The lab provided practical exposure to identifying potentially relevant indicators from security evidence.

Important IOC categories include:

- IP addresses
- Domains
- URLs
- File hashes
- Suspicious processes
- Other security-relevant artifacts

A key lesson was that an observed artifact should not automatically be treated as malicious without supporting evidence.

---

## 7. Evidence-Based Investigation

Security investigations should be based on available evidence rather than assumptions.

A useful approach is:

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

This helps reduce unsupported conclusions during incident investigation.

---

## 8. Defensive Security Mindset

The lab reinforced the importance of thinking from a defensive perspective.

Instead of focusing only on how an attack works, the investigation process considers:

- How the activity appears in telemetry
- How it can be detected
- What evidence it produces
- How an analyst can investigate it
- Which indicators can support the investigation
- How the findings should be documented

---

## 9. Practical SOC Workflow

The lab helped connect individual cybersecurity technologies with a broader SOC workflow.

```text
Technology
    |
    v
Telemetry
    |
    v
Detection
    |
    v
Investigation
    |
    v
IOC Analysis
    |
    v
Incident Understanding
```

This provided a practical understanding of how different security components contribute to security operations.

---

## 10. Key Takeaways

The main lessons from the project were:

- Security monitoring requires multiple sources of visibility
- Network and endpoint telemetry complement each other
- Alerts require investigation and context
- Evidence should be correlated before drawing conclusions
- IOC analysis supports incident investigation
- Documentation is an important part of SOC operations
- A controlled home lab can provide practical experience with defensive security workflows

---

## Future Improvements

If the lab is rebuilt in the future, possible improvements include:

- Centralized log collection
- SIEM integration
- Additional endpoint telemetry
- More detection use cases
- Automated alerting
- Structured incident response playbooks
- Additional attack simulations
- Detection rule development
- Automated IOC enrichment
- Improved dashboarding and visualization

---

## Final Reflection

The SOC home lab provided a practical environment for connecting security tools, telemetry, detection, and investigation into a single defensive workflow.

The most important takeaway was understanding that effective SOC analysis depends not only on detecting suspicious activity, but also on collecting evidence, correlating multiple data sources, investigating the activity, extracting relevant indicators, and documenting the findings.
