# Participant Briefing — Operation Foggy Key

**Date of incident:** Sept 20, 2025 (simulated)  
**Environment:** Small company running workloads in AWS.  
**Business context:** Customer PII in `s3://acme‑cust‑data`. Revenue‑critical ETL on EC2.

## What you know at T+0
- An alert claims unusual AWS Console sign-ins without MFA for user **alex.old**.
- A cost anomaly shows a sudden EC2 spend spike.
- Customers reported slow API responses in the last 24 hours.

## Objectives
1) **Threat Identification:** Determine what happened, to whom, and how far it spread.  
2) **Containment:** Stop active malicious activity and protect critical assets.  
3) **Eradication:** Remove attacker access, remediate persistence, and outline recovery steps.

## Rules of engagement
- This is a tabletop: you’ll reason and decide based on artifacts (no real prod changes).  
- Use the provided evidence pack under `evidence/`.  
- Prioritize safety of data and business continuity.
