# IT Security Audit — Botium Toys

## Objective

Botium Toys is a small U.S. retail and e-commerce business that has grown an international customer base, including in the E.U., without a corresponding update to its security and compliance posture. The IT manager requested an internal audit to identify gaps in controls and regulatory compliance before those gaps translate into fines or a breach. My task: review the company's asset inventory and risk assessment, then complete a full controls and compliance audit with prioritized recommendations.

## Scope

The audit covered the entirety of Botium Toys' IT-managed assets: employee equipment, the internal network, e-commerce and payment systems, data storage and retention, and legacy system maintenance. Two regulatory contexts applied directly: PCI DSS (the company processes credit card payments) and GDPR (the company serves E.U. customers).

## Framework

I applied the **NIST Cybersecurity Framework (CSF)**, starting from the Identify function — establishing what assets exist and what the impact of losing them would be — before assessing controls and compliance against that asset baseline.

## Process

1. Reviewed the existing scope, goals, and risk assessment report to understand the company's current asset inventory and stated risk posture
2. Assessed the risk score using likelihood and impact reasoning specific to Botium Toys' size, customer base, and international exposure — the report assigns a risk score of **8/10**, driven primarily by the volume of missing controls relative to the company's compliance obligations
3. Completed a controls assessment checklist across 14 security controls (least privilege, disaster recovery, password policy, separation of duties, firewall, IDS, backups, antivirus, legacy system monitoring, encryption, password management, physical security controls)
4. Completed a compliance checklist against three frameworks: **PCI DSS**, **GDPR**, and **SOC (Type 1/2)**
5. Wrote prioritized recommendations tied to the specific gaps identified, rather than a generic best-practices list

## Key findings

**In place:** firewall, antivirus software, physical security controls (locks, CCTV, fire detection), a GDPR breach-notification plan, and enforced data-integrity/privacy policies.

**Missing:** least privilege and separation of duties (all employees currently have broad access to cardholder data and customer PII/SPII), encryption of stored credit card data, an intrusion detection system, disaster recovery planning and backups, and a centralized password management system — the existing password policy doesn't meet current complexity standards.

The compliance gaps compound the control gaps: without least privilege, encryption, or a breach-ready backup process, Botium Toys is exposed under both PCI DSS and GDPR despite having some baseline protections in place.

## Recommendations delivered

Prioritized by risk reduction per effort: implement least privilege and separation of duties first (no new tooling required, immediate exposure reduction), then password policy enforcement and a password management system, followed by encryption of stored payment data, IDS deployment, and a formal backup/disaster recovery plan with a defined legacy-system monitoring schedule.

## What I'd do differently

I'd push for a follow-up control — a defined review cadence (e.g., quarterly) for the controls checklist itself, since a one-time audit doesn't catch drift as the company keeps growing internationally. I'd also want to quantify the recommendations against something Botium Toys' management would weigh directly, like estimated GDPR fine exposure versus the cost of implementing encryption, to make the prioritization easier for a non-technical stakeholder to approve.

## Tools & concepts

NIST CSF · PCI DSS · GDPR · SOC 1/SOC 2 · Risk scoring · Controls assessment · Least privilege · Separation of duties
