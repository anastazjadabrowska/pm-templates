# PRD TEMPLATE: Trust & Safety Tooling for Market Expansion
**Status:** `[Draft / In Review / Shipped]`
**Author:** `[PM name]`
**Market:** `[e.g. CZ, SK, HU]`
**Last updated:** `[date]`

---

## Problem

Expanding the platform to a new market requires adapting Trust & Safety tools to local regulations, languages, and product rules. Without a repeatable, documented process, each expansion starts from scratch — creating inconsistency, delays, and knowledge loss between rollouts.

The same questions come up every time:
- How do we handle currency conversion in fraud detection logic?
- What product categories are restricted or prohibited in this country?
- How do we adapt content moderation for a new language?

**Market-specific context:**
> `[Describe why this market, what triggered the expansion, and any known constraints or regulatory specifics.]`

---

## High Level Approach

Use this template as the single source of truth for each expansion. Every decision, open question, and sign-off is documented here — not in Slack, not in someone's head.

Each checklist item maps to a Jira ticket. No ticket closed = no item complete.

---

## OKRs

**Objective:** Successfully expand T&S tooling to `[market]` with no increase in fraud rate and full regulatory compliance at launch.

| Key Result | Target | Measurement |
|------------|--------|-------------|
| T&S tools ready before market launch | 100% checklist complete T-2 weeks | Jira tickets closed |
| Fraud rate in new market ≤ existing market average | ≤ `[X]`% at 90 days | Analytics dashboard |
| Escalations caused by missing localization rules | 0 critical in first 30 days | Ops incident log |
| Regulatory sign-off obtained | Legal approval documented | Decision log in this PRD |

---

## Narrative

**Today (without this playbook):**
A new market is announced. The T&S PM scrambles to identify what needs to change — currency rules, prohibited categories, language adaptation. They ask the same questions that were asked during the previous expansion. Answers are buried in Slack threads, old tickets, or the memory of a colleague who may no longer be on the team.

**With this playbook:**
A new market is announced. The PM opens this template, works through each section with legal, compliance, data, and localization, and documents all decisions inline. The next expansion takes half the time.

---

## Non-goals

- We are not rebuilding the T&S tooling architecture for each market
- We are not automating the expansion process end-to-end
- We are not handling payment localization — owned by a separate team
- `[Add market-specific non-goals]`

---

## Expansion Checklist

Each item below = one Jira ticket. Ticket must be closed before moving to the next phase.

### 1. Currency & Financial Rules
- [ ] Define how currency conversion affects fraud thresholds — Jira: `[TICKET-ID]`
- [ ] Confirm local payment methods and associated risk profiles — Jira: `[TICKET-ID]`
- [ ] Validate fraud detection rules are calibrated for local GMV levels — Jira: `[TICKET-ID]`

### 2. Product Category Rules
- [ ] Review prohibited and restricted product categories per local law — Jira: `[TICKET-ID]`
- [ ] Map to existing platform category taxonomy — Jira: `[TICKET-ID]`
- [ ] Flag edge cases for legal review — Jira: `[TICKET-ID]`

### 3. Language & Content Moderation
- [ ] Identify language support requirements (moderation, UI strings, alerts) — Jira: `[TICKET-ID]`
- [ ] Confirm availability of moderation tooling for the language — Jira: `[TICKET-ID]`
- [ ] Define escalation path for content that cannot be auto-moderated — Jira: `[TICKET-ID]`

### 4. Regulatory & Compliance
- [ ] Identify country-specific regulatory requirements — Jira: `[TICKET-ID]`
- [ ] Confirm reporting obligations to local authorities — Jira: `[TICKET-ID]`
- [ ] Update DPIA if new data processing activities introduced — Jira: `[TICKET-ID]`

### 5. Stakeholder Sign-off
- [ ] Legal — Jira: `[TICKET-ID]`
- [ ] Compliance — Jira: `[TICKET-ID]`
- [ ] Data / Analytics — Jira: `[TICKET-ID]`
- [ ] Operations (T&S team leads) — Jira: `[TICKET-ID]`
- [ ] Localization — Jira: `[TICKET-ID]`

---

## Decision Log

All significant decisions documented here. Format:

> **[Decision]** `[What was decided]`
> **Rationale:** `[Why]`
> **Alternatives considered:** `[What else was on the table]`
> **Owner:** `[name]` | **Date:** `[date]` | **Reviewed by:** `[Legal / Data / other]`

*Example:*
> **[Decision]** Apply the same fraud threshold as the PL market for the first 90 days, then recalibrate based on local data.
> **Rationale:** Insufficient local data at launch to set independent thresholds.
> **Alternatives considered:** Set conservative (higher) thresholds from day 1 — rejected due to expected high false positive rate.
> **Owner:** PM | **Date:** 2024-01-15 | **Reviewed by:** Legal, Data

---

## Open Questions

| Question | Owner | Due date | Status |
|----------|-------|----------|--------|
| `[Question]` | `[name]` | `[date]` | Open / Resolved |

---

## Launch Plan

| Phase | Goal | Exit Criteria | Jira Epic |
|-------|------|---------------|-----------|
| 1 — Checklist review | Identify all gaps | All sections reviewed, owners assigned | `[EPIC-ID]` |
| 2 — Localization & rules | Adapt tools to local context | Legal & compliance sign-off | `[EPIC-ID]` |
| 3 — Pilot | Soft launch with monitoring | No critical incidents in first 14 days | `[EPIC-ID]` |
| 4 — Full launch | Market live | KPIs within range at 30 days | `[EPIC-ID]` |

**Risks:**

| Risk | Likelihood | Impact | Mitigation |
|------|------------|--------|------------|
| Regulatory requirements unclear at launch | Medium | High | Engage legal early; document open questions |
| Moderation tooling doesn't support language | Low | High | Validate in Phase 1 |
| Fraud patterns differ significantly from baseline | Medium | Medium | 90-day recalibration checkpoint |
| `[Add market-specific risks]` | | | |

---

## Key Milestones

| Milestone | Owner | Target date | Jira ticket |
|-----------|-------|-------------|-------------|
| Template filled for this market | PM | T-8 weeks | `[TICKET-ID]` |
| Legal & compliance sign-off | Legal | T-4 weeks | `[TICKET-ID]` |
| Tools adapted and tested | Engineering | T-2 weeks | `[TICKET-ID]` |
| Checklist 100% complete | PM | T-2 weeks | `[TICKET-ID]` |
| Pilot launch | PM + Ops | T-0 | `[TICKET-ID]` |
| 30-day OKR review | PM + Data | T+30 days | `[TICKET-ID]` |
| 90-day OKR review | PM + Data | T+90 days | `[TICKET-ID]` |

---

## How We Verify Changes Were Introduced

**Rule:** Nothing is "done" until the Jira ticket is closed.

- Every checklist item above has a corresponding Jira ticket
- Tickets are reviewed in sprint planning and weekly syncs
- This document is linked in the Jira epic description — it is the single source of truth
- Before moving from Phase 1 → Phase 2, all Phase 1 tickets must be closed
- 30-day and 90-day OKR reviews are scheduled at kickoff, not retroactively

**Audit trail:**
- Decisions documented in Decision Log above with date and owner
- Open questions tracked until resolved — no question disappears without an answer on record
- Document version history maintained; major changes noted below

---

## Changelog

| Version | Date | Change | Author |
|---------|------|--------|--------|
| 1.0 | `[date]` | Initial template created | `[PM]` |
| `[x.x]` | `[date]` | `[what changed]` | `[name]` |

---

*This is an anonymized template based on real work at a large e-commerce platform. Sensitive business data has been removed or generalized. Built to be reusable across market expansions.*
