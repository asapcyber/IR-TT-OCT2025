# 2‑Hour Cyber Incident Response Table‑Top Exercise (TTX) Kit

**Scenario:** *Operation Foggy Key* — An old IAM user's access key is exposed. An attacker performs suspicious console logins, spins up EC2 instances for crypto‑mining, opens a security group to the world, and accesses sensitive S3 data. You must **Identify**, **Contain**, and **Eradicate**.

## What’s included
- `IncidentBriefing.md` (participant handout)
- `FacilitatorGuide.md` (step‑by‑step with prompts and answers)
- `msel.csv` (Master Scenario Events List / inject timeline)
- `scorecard.csv` (evaluation & scoring checklist)
- `event_log_template.csv` (scribe logging template)
- Evidence (under `evidence/`):
  - `cloudtrail_logs.jsonl`
  - `vpc_flow_logs.csv`
  - `guardduty_findings.jsonl`
  - `iam_credential_report.csv`

## Minimal tooling
Open CSV/JSON in any spreadsheet or text editor. Optionally use local tools (jq, Excel filters, Wireshark for CSV exploration, CyberChef) — **no full cyber range required**.

## Roles (suggested for ~10 people)
Incident Lead, Blue Team Lead, Cloud Sec Lead, Forensics, SOC Analyst, Threat Intel, IT Ops, Comms/Legal Liaison, Timekeeper, Scribe. Remote observers can watch the shared screen and add comments in chat.

## Timebox (120 minutes)
- 0–10: Briefing & rules
- 10–25: Initial indicators (ID phase)
- 25–60: Pivoting & scoping (ID → Containment)
- 60–95: Containment actions
- 95–110: Eradication & recovery plan
- 110–120: Hotwash (quick debrief) & action items

See `FacilitatorGuide.md` for prompts, pacing, and answer key hints.
