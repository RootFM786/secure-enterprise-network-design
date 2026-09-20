# Security Controls and Threats

## Threat-to-Control Mapping

| Threat | Controls Proposed in Original Design | Analyst Signal |
|---|---|---|
| Unauthorised access | User accounts, access restrictions, ACLs, staff awareness | Repeated denied connections, unexpected authentication activity |
| Insider misuse | Segmentation, least-access concepts, monitoring of remote connections | Access to unusual departments or sensitive resources |
| Malware | Mail filtering, gateway inspection, endpoint anti-malware, patching | Suspicious outbound connections, endpoint alerts, abnormal process/network behaviour |
| DDoS | Bandwidth headroom, rate limiting, filtering, connection controls | Large traffic spikes, service degradation, unusual source distribution |
| Physical compromise | Restricted server-room access and building access controls | Physical-access events correlated with system changes |
| Third-party risk | Separate subnet, ACLs and separate internet path | Cross-boundary traffic from the rented-floor environment |

## Layered Security

The group design did not rely on a single control. It combined:

- segmentation
- firewalling
- ACLs
- endpoint protection
- staff policies and awareness
- physical security
- backups
- monitoring

This layered approach is important because no single control prevents every attack.

## Current Reflection

Today I would make the control design more measurable by defining:

- expected allowed flows
- logging requirements per control
- alert conditions
- control owner
- review frequency
- failure / bypass scenarios