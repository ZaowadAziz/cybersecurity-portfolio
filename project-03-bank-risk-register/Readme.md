# Risk Register — Commercial Bank

## Objective

A commercial bank's cybersecurity team needed to prioritize a set of identified risks to its assets. My task, as a member of that team, was to score each risk by likelihood and severity, calculate an overall priority score, and produce reasoning the team could use to decide where to focus limited security resources first.

## Operational context

The bank operates in a low-crime coastal area with 100 on-premise and 20 remote employees, serving roughly 2,000 individual and 200 commercial accounts, with strict federal cash-reserve and financial-data regulations to meet. Context matters here — a generic risk register ignores the fact that this bank's specific exposure comes from its remote workforce and customer data volume, not from its physical environment.

## Method

Used a standard likelihood × severity scoring model (each rated 1–3, multiplied for a priority score up to 9) against five identified risks to the bank's core asset — customer and institutional funds.

| Risk | Description | Likelihood | Severity | Priority |
|---|---|---|---|---|
| Financial records leak | A backup database server is publicly accessible | 3 | 3 | **9** |
| Compromised user database | Customer data is poorly encrypted | 2 | 3 | 6 |
| Business email compromise | An employee is tricked into sharing confidential information | 2 | 2 | 4 |
| Theft | The bank's physical safe is left unlocked | 1 | 3 | 3 |
| Supply chain disruption | Delivery delays from natural disasters | 1 | 2 | 2 |

## Reasoning

The bank's low-crime location genuinely lowers physical theft risk, but that same reasoning doesn't extend to digital risk — a large customer base raises the severity of any data leak regardless of the neighborhood, and the 20 remote employees represent the highest-likelihood attack surface since they operate outside the bank's direct network controls. The publicly-accessible backup server scored highest priority specifically because it combines high likelihood (it's already exposed, not theoretical) with high severity (financial records, not just PII).

## Key finding

The highest-scored risk (the exposed backup server) is also the cheapest to fix — access control on a server that shouldn't be public in the first place — while the lowest-scored risk (supply chain disruption) would require the most resource investment to meaningfully mitigate. That gap is the actual output a risk register should surface: not just a ranked list, but where effort-to-impact ratio favors immediate action.

## What I'd do differently

I'd add a fourth axis beyond likelihood and severity — remediation cost — since two risks with the same priority score can have very different cases for urgency once cost is factored in. I'd also revisit this register on a defined cycle rather than as a single point-in-time exercise, since the remote-employee risk profile in particular will shift as the bank's staffing changes.

## Tools & concepts

Risk assessment methodology · Likelihood × severity scoring · Risk prioritization · Asset-based risk analysis · Financial sector compliance context
