# IT0123 DevNet Resource Validation Plan

## Student and Project

- Name: Rommel A Mercado
- Section: TN32
- Repository name: `it0123-devnet-resource-plan`

## Purpose

Choosing the correct DevNet resource before starting a network-automation
task avoids wasted setup time, prevents accidentally attempting
administrative work on a shared environment, and ensures the access model
(instant, scheduled, or code-only) actually matches what the task requires.
Getting this wrong either blocks the work (e.g., trying to reconfigure a
device on a shared Always-On Sandbox) or wastes a reservation window that
could have been avoided with a Learning Lab or Code Exchange search instead.

## Validated Resource Decisions

| Use Case | Selected Resource | Key Requirement | Official Evidence |
|---|---|---|---|
| UC1 — Quick read-only API exploration | `always-on-sandbox` | Immediate, no-wait, non-admin access | https://developer.cisco.com/docs/sandbox/ |
| UC2 — Private configuration testing | `reservation-sandbox` | Private, administrative access; VPN/setup acceptable | https://developer.cisco.com/docs/sandbox/faqs/ |
| UC3 — Guided API concept practice | `learning-lab` | Structured, step-by-step learning before independent work | https://developer.cisco.com/learning/ |
| UC4 — Reusable automation example | `code-exchange` | Reviewing existing repositories before building new automation | https://developer.cisco.com/codeexchange/ |

Full rationale, AI recommendation summaries, and verification status for each
entry are in `student_plan.json`.

## AI Evaluation

Two of the four AI recommendations needed correction before they could be
accepted as-is:

- **UC2:** The AI correctly identified `reservation-sandbox` but did not
  state a concrete setup-time figure. The official Sandbox FAQ was used to
  add that reservation sandboxes typically take 15–45 minutes to provision,
  which is relevant to whether the team's schedule can accommodate it.
- **UC4:** The AI initially used the outdated name "Automation Exchange."
  Official Cisco documentation confirms Automation Exchange was consolidated
  into Cisco Code Exchange, so the recommendation was corrected to
  `code-exchange` before it was accepted.

UC1 and UC3 were verified as given, with no corrections needed.

See `ai_prompt_transcript.md` for the full prompt and response record for
all four scenarios.

## Validation Evidence

- Validator result: **VALIDATION COMPLETE: 9/9 checks passed** (see
  `validator_result.txt`)
- Command used: `python validate_plan.py`
- Official Cisco pages reviewed:
  - https://developer.cisco.com/docs/sandbox/
  - https://developer.cisco.com/docs/sandbox/faqs/
  - https://developer.cisco.com/learning/
  - https://developer.cisco.com/codeexchange/

## Git Evidence

- Initial commit message: `Initial commit: add starter files and README for IT0123 Module 2 DevNet resource plan`
- Validation commit message: `Complete validated student_plan.json, README, and validator evidence (9/9 checks passed)`
- Output of `git log --oneline`: see below, regenerated after the second commit.

```
e667331 Complete validated student_plan.json, README, and validator evidence (9/9 checks passed)
f4d6853 Initial commit: add starter files and README for IT0123 Module 2 DevNet resource plan
```

## AI-Use Disclosure

- **AI tool used:** Claude (Anthropic)
- **Type of assistance received:** For each of the four fictional use cases,
  Claude was asked to recommend exactly one DevNet resource type, give the
  driving requirement, and state a verifiable claim about access, isolation,
  setup, or privileges (per the suggested prompt in the assignment).
- **What was independently checked:** Every recommendation was checked
  against official Cisco documentation at `developer.cisco.com` (Sandbox
  docs/FAQ, Learning Labs, Code Exchange) before being accepted.
- **What was revised:** The UC2 rationale was expanded with a specific
  setup-time range from the official FAQ, and the UC4 resource label was
  corrected from the AI's outdated "Automation Exchange" term to the current
  "Code Exchange" terminology. No usernames, passwords, tokens, or personal
  data were shared with the AI at any point.
