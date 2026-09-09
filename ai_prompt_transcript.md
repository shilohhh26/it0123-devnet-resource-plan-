# AI Prompt Record — IT0123 Module 2 DevNet Resource Validation

AI tool used: Claude (Anthropic). No credentials, usernames, tokens, or personal
data were shared with the AI at any point. Only the fictional use cases from
`devnet_use_cases.json` were used.

---

## UC1 — Quick read-only API exploration

**Prompt sent:**
> I am selecting a Cisco DevNet resource for a fictional classroom use case.
> Use case: A student team needs immediate access to a shared Cisco environment
> to practice safe read-only API requests. Administrative changes are not
> required, and the team cannot wait for provisioning.
> Choose exactly one: learning-lab, always-on-sandbox, reservation-sandbox, or
> code-exchange. Explain which requirement drove your choice. State any access,
> isolation, setup, or privilege claim that I should verify in official Cisco
> documentation. Do not invent a sandbox product name, URL, account, or
> credential.

**AI response (summary):** Recommended `always-on-sandbox`. Driving
requirement: immediate access with no provisioning wait. Claim to verify:
Always-On Sandboxes are shared, available instantly, and restrict
administrative access.

**Independent verification:** Confirmed against `developer.cisco.com/docs/sandbox/`
— status: verified.

---

## UC2 — Private configuration testing

**Prompt sent:**
> I am selecting a Cisco DevNet resource for a fictional classroom use case.
> Use case: A development team must test configuration changes with
> administrative access in a private environment. The team can schedule
> access, use a VPN, and accept setup time.
> Choose exactly one: learning-lab, always-on-sandbox, reservation-sandbox, or
> code-exchange. Explain which requirement drove your choice. State any access,
> isolation, setup, or privilege claim that I should verify in official Cisco
> documentation. Do not invent a sandbox product name, URL, account, or
> credential.

**AI response (summary):** Recommended `reservation-sandbox`. Driving
requirement: private, administrative access for configuration testing.
Claim to verify: reservation sandboxes are private and require VPN and setup
time.

**Independent verification:** Confirmed against `developer.cisco.com/docs/sandbox/faqs/`
— the AI did not mention a specific setup-time range, so I added the
"15–45 minutes" figure from the FAQ myself. Status: partially-verified.

---

## UC3 — Guided API concept practice

**Prompt sent:**
> I am selecting a Cisco DevNet resource for a fictional classroom use case.
> Use case: A beginner needs structured, step-by-step learning content before
> attempting an independent API activity. The immediate goal is guided
> practice rather than access to administrative devices.
> Choose exactly one: learning-lab, always-on-sandbox, reservation-sandbox, or
> code-exchange. Explain which requirement drove your choice. State any access,
> isolation, setup, or privilege claim that I should verify in official Cisco
> documentation. Do not invent a sandbox product name, URL, account, or
> credential.

**AI response (summary):** Recommended `learning-lab`. Driving requirement:
guided, self-paced instruction, not an execution environment.

**Independent verification:** Confirmed against `developer.cisco.com/learning/`
— status: verified.

---

## UC4 — Reusable automation example

**Prompt sent:**
> I am selecting a Cisco DevNet resource for a fictional classroom use case.
> Use case: A developer wants to examine community and Cisco-maintained code
> repositories for an existing network-automation use case before designing a
> new solution.
> Choose exactly one: learning-lab, always-on-sandbox, reservation-sandbox, or
> code-exchange. Explain which requirement drove your choice. State any access,
> isolation, setup, or privilege claim that I should verify in official Cisco
> documentation. Do not invent a sandbox product name, URL, account, or
> credential.

**AI response (summary):** Initially recommended "Automation Exchange" for
reviewing existing repositories before building new automation.

**Independent verification:** `developer.cisco.com/codeexchange/` and the
related Automation Exchange page confirm Automation Exchange has been
consolidated into Cisco Code Exchange. I corrected the AI's label to
`code-exchange` per current Cisco terminology. Status: partially-verified.
