# Phase 1: Requirement gathering

**Goal:** Know exactly what is being built, why, for whom at a business level, and
what limits apply. Everything later depends on this.

**Done when:** The problem, goals, success measures, scope and constraints are all
specific enough that two developers reading them would build the same thing.

## If a BRD exists

Extract everything it says into the spec first. Then list the gaps and
contradictions you found and grill only on those, plus anything below the BRD
doesn't cover. Never re-ask what the BRD answers clearly.

## If starting from an idea

Grill on everything below. Expect more batches.

## Question areas

**Problem and purpose**
- What problem does this solve? What happens today without it?
- What triggers the need (a complaint, lost revenue, manual effort, a customer ask)?
- Ask for a concrete recent example of the problem happening.

**Goals and success**
- Business goals (reduce calls, faster turnaround, fewer errors, new revenue).
- How success will be measured, with numbers and a timeframe where possible.
- What would make this project a failure?

**Users at a high level**
- Which groups will use it (internal staff, customers, partners, admins)?
- Roughly how many of each? (Details come in phase 2.)

**Scope**
- Features that must be in the first release.
- Features explicitly out of scope, and features planned for later.
- For each must-have, ask what happens if it is cut. This tests whether it's real.

**Constraints**
- Timeline, budget, team size.
- Technology: existing systems, required stack, hosting.
- Integrations: which systems it reads from or writes to (ERP, CRM, accounting,
  email, payments). Which system is the source of truth for each piece of data?
- How fresh does data need to be (real time, hourly, daily)?
- Legal, compliance and privacy: personal data, data retention, audit trails,
  industry rules, data residency.
- Security: login method (password, SSO, OTP), session length, multi-factor.

**Platform and context**
- Devices: desktop, tablet, mobile (default all three).
- Web app, native app, or both?
- Languages and regions: localisation, currency, date formats, time zones.
- Connectivity: will anyone use it with poor or no internet?

**Volumes**
- Number of records users will deal with (10 orders or 10,000?). This decides
  search, filters and pagination later.
- Expected growth.

**Stakeholders and risks**
- Who signs off on the UX? Who else must be consulted?
- Biggest risks or unknowns as the person sees them.

## Traps to probe

- "Everything is must-have": force a ranking.
- "Real time" without a reason: ask what breaks if data is 15 minutes old.
- Integrations named but not understood: ask what happens when the other system is
  down or slow.
- Hidden users: who approves, who supports, who administers?

## Spec section 1 structure

1.1 Problem statement · 1.2 Goals and success measures · 1.3 Users (high level) ·
1.4 Scope (in, out, later) · 1.5 Constraints · 1.6 Integrations and data sources ·
1.7 Platforms, languages and regions · 1.8 Volumes · 1.9 Stakeholders · 1.10 Risks
