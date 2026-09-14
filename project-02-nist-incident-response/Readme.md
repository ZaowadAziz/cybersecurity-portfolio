# Incident Response Analysis — ICMP Flood (DoS) Attack

## Objective

A multimedia company offering web design, graphic design, and social media services experienced a denial-of-service attack that took its internal network offline for two hours. As the cybersecurity analyst reviewing the incident, my task was to analyze the event and build a forward-looking response strategy using the NIST Cybersecurity Framework, rather than just documenting what happened.

## Incident summary

A malicious actor exploited an unconfigured firewall to flood the company's network with ICMP ping packets, overwhelming it and causing a two-hour outage of internal network resources. The incident response team's immediate action was to block incoming ICMP packets, take non-critical services offline, and restore critical services — but the underlying firewall misconfiguration was the real point of failure.

## Framework

I structured the analysis around all five NIST CSF functions rather than stopping at "what we did to stop it," since a durable fix requires covering detection and recovery too, not just the immediate response.

| Function | Analysis |
|---|---|
| **Identify** | The attack vector was an ICMP flood exploiting a firewall with no rate-limiting rule in place — the root cause was a configuration gap, not a zero-day. |
| **Protect** | Configured the firewall to rate-limit incoming ICMP traffic and added an IDS/IPS filter to block suspicious traffic patterns going forward. |
| **Detect** | Recommended source IP verification on the firewall to catch spoofed addresses, plus network monitoring software to flag abnormal traffic before it escalates to an outage. |
| **Respond** | Documented a playbook: isolate the attack to prevent spread, investigate logs to trace origin, adjust firewall/monitoring configuration, and report findings to upper management. |
| **Recover** | Defined a recovery sequence — restore critical services first, keep non-critical services offline until ICMP traffic times out, then bring non-critical services back online in a controlled order. |

## Key finding

The core issue wasn't the attack itself — ICMP floods are a well-understood, low-sophistication attack type. The real gap was that firewall configuration hadn't been reviewed or hardened proactively, which meant a basic attack had an outsized impact. That's a process failure (no regular firewall rule review) as much as a technical one.

## What I'd do differently

I'd tie the "Respond" playbook to a defined SLA (e.g., time-to-isolate, time-to-restore-critical-services) so the response has a measurable target next time, not just a sequence of steps. I'd also recommend the firewall review become a scheduled control rather than a reactive one — the same gap that caused this incident will recur under a different attack type if configuration review stays ad hoc.

## Tools & concepts

NIST CSF (Identify–Protect–Detect–Respond–Recover) · Denial-of-Service (DoS) attacks · Firewall configuration · IDS/IPS · Incident playbooks · Network monitoring
