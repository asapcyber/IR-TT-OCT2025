# Facilitator Guide — Operation Foggy Key

## Setup
- Share screen with `msel.csv`, evidence files, and `scorecard.csv` visible.
- Assign roles and confirm scribe & timekeeper.
- Start a meeting recording (room mic) and let remote observers join video.

## Script (high-level)
- **T+0** Read the Participant Briefing.
- **Inject 1 (T+5):** Unusual ConsoleLogin without MFA (cloudtrail excerpt).
  - *Prompt:* What is your first hypothesis? What logs do you want next?
  - *Expected:* Identify user `alex.old`, source IP, region, and timeframe.
- **Inject 2 (T+12):** Cost spike + GuardDuty finding (CryptoMining on EC2).
  - *Prompt:* Which instances, accounts, and security groups are involved?
  - *Expected:* Scope suspicious EC2, open SG to 0.0.0.0/0 (SSH).
- **Inject 3 (T+25):** S3 access attempts on `acme-cust-data` and policy changes.
  - *Prompt:* What data is at risk? Evidence of exfiltration?
  - *Expected:* Detect S3 GetObject calls and related IAM changes.
- **Inject 4 (T+45):** Persistence indicators (new access key, policy attach).
  - *Prompt:* How do you contain without data loss?
  - *Expected:* Key disable/rotate, SG restrict, isolate/quarantine instances.
- **Inject 5 (T+70):** Business owner requests ETA and comms plan.
  - *Prompt:* What’s the containment status and customer impact message?
  - *Expected:* Clear, non-technical summary & initial timeline.
- **Inject 6 (T+95):** Final sweep: enumerate backdoors and recovery plan.
  - *Expected:* Remove keys/policies, review CloudTrail, GuardDuty, VPC logs, confirm no egress.

## Scoring
Use `scorecard.csv` (0–3 scale): 0=missed, 1=late/partial, 2=good, 3=exemplary with rationale.

## Debrief
- What would you automate or detect earlier next time?
- Immediate action items (owners & deadlines).

*Answer key hints are embedded in `msel.csv` “Evaluation Notes/Hints”.*
