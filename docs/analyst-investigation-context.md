# Analyst Investigation Context

## Why Network Design Matters During Triage

A network diagram is not just documentation for network engineers. It gives a security analyst the context needed to decide whether an event is suspicious.

## Example 1 — Cross-VLAN Connection

**Alert:** A workstation in Sales initiates connections to a server in a restricted Finance segment.

Questions an analyst should ask:

1. Is Sales permitted to reach Finance?
2. Which ACL or firewall rule allowed the traffic?
3. Is the destination normally accessed by this user or device?
4. Is the source host showing other signs of compromise?
5. Are there similar attempts toward other internal segments?

This turns a raw network event into a possible **lateral-movement investigation**.

## Example 2 — DMZ to Internal Network

**Alert:** A public-facing web server begins making unexpected outbound connections to internal systems.

Why it matters:

- DMZ systems are exposed to more external risk
- internal connections from them should be tightly controlled
- unexpected internal communication may indicate post-compromise movement

## Example 3 — Third-Party Network

**Alert:** Traffic from the rented-floor network is observed attempting to reach corporate user VLANs.

The original design intended that environment to remain isolated. That architectural expectation gives the analyst an immediate reason to investigate.

## Example 4 — Availability vs Security

A network outage is not automatically a cyberattack.

Because the design includes redundant links, STP and backup devices, an analyst should consider:

- link or device failure
- STP / switching issues
- routing failure
- DDoS
- deliberate configuration change

Understanding resilience mechanisms helps avoid misclassifying infrastructure faults as malicious activity.

## Core Takeaway

Security monitoring becomes much more useful when analysts know the **expected network path, trust boundary and permitted communication**.