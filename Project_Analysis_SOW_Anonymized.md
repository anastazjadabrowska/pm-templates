# Project Analysis & SOW: Mobile Marketplace App
**Author:** Nastka Dąbrowska
**Context:** Analysis for an external client of a software house — project status assessment, requirements analysis, and effort estimation.

---

## TL;DR

The project is in critical delay — **10% completion at ~33% elapsed time**. Key risks: design and architecture phases not started, no PM assigned, cascading delays imminent. Recommended: immediate PM assignment, internal stabilization, crisis meeting with client, and schedule revision.

---

## 1. Project Status Assessment & Recommendations

### 1.1 Identified Problems

**Problem 1: Critical delay in analysis & design phase**
- Mockups — planned completion passed → **0% done**
- Graphic design — cannot start without mockups → **0%**
- Architecture — planned completion passed → **0%**
- Development scheduled to start is **fully blocked**

**Impact:** Very high risk of cascading delay across the entire project.

**Problem 2: No Project Manager assigned**
- Resource plan shows PM at 100% allocation, **0 hours logged**
- At 562h total project scope, missing PM means no escalation, no coordination

**Problem 3: Resource allocation inconsistencies**

| Role | Schedule (WBS) | Resource Plan | Delta |
|------|---------------|---------------|-------|
| Developer Android | 116h | 24h | ⚠️ -92h |
| Developer iOS | 116h | 136h | +20h |
| Tester | 24h | 136h | ⚠️ +112h |

Source data is inconsistent — must be corrected before further planning.

**Problem 4: Contract not signed**
- Contract signing: **50% complete**, deadline passed
- **Risk:** Continuing work without signed contract creates legal and financial exposure

**Problem 5: Unrealistic dependencies in schedule**
- Development (iOS/Android) scheduled to start with dependency on Architecture
- Architecture not started, Specification only 50% complete
- Schedule does not reflect actual work sequence

*These problems indicate simultaneous schedule, resource, and decision-making risk — requiring a systemic response, not point fixes.*

---

### 1.2 Project Health Summary

| Area | Status |
|------|--------|
| Overall progress | 10% (vs ~33% expected) |
| Schedule | Critical delay (min. 3-5 days) |
| Budget | Unused; high risk of overrun |
| Team | Unbalanced resource allocation |
| Risk | **HIGH — immediate intervention required** |

---

### 1.3 Recommended Actions

**Action 1: Assign Project Manager (immediate)**
- Temporary/conditional assignment if possible without client escalation
- Recommended initial allocation: 20–30% during stabilization phase
- Scope: schedule, risks, communication, team coordination
- Deadline: immediately

**Action 2: Internal project stabilization**
- Verify and align data (schedule vs. resources)
- Identify actual critical path
- Confirm contract status
- Prepare at least two realistic scenarios:
  - Full scope with revised timeline
  - Reduced scope (MVP)
- Deadline: within 1-2 days

**Action 3: Crisis meeting with client**
- Present real project status transparently
- Present prepared scenarios
- Jointly decide on scope, timeline, and next steps
- Establish basis for contract decisions
- Deadline: within 2 days of internal stabilization

**Action 4: Resolve contract & formal matters**
- Confirm scope and terms of continued cooperation
- Sign contract or amendment
- Deadline: within 3 days

**Action 5: Update schedule and dependencies**
Corrected dependency sequence:
**Specification → Architecture → Mockups → Graphic Design → Development**

Revised end dates:
- Full scope: +8-10 days from original
- MVP: +3-5 days from original

**Action 6: Correct resource allocation**
- Increase Developer Android allocation to match schedule
- Reduce or reschedule Tester allocation
- Consider additional Designer support in design phase

**Action 7: Establish working rhythm**
- Daily stand-up (15 min)
- Checkpoints every 48h during critical phases
- Definition of Done for key deliverables
- Client feedback SLA: max 3 business days

---

### 1.4 Key Risks & Mitigations

| Risk | Impact | Mitigation |
|------|--------|------------|
| No PM assigned | High | Immediate allocation |
| Unsigned contract | High | Formal decision + escalation |
| Inconsistent resource data | Medium | Data correction |
| Client acceptance delays | Medium | Feedback SLA (3 days) |

---

## 2. Client Requirements Analysis

### 2.1 Functional Requirements Summary

1. User registration and login
2. Add, edit, and browse listings
3. Send inquiries + push notifications
4. Automatic listing expiration
5. Paid listing extension

### 2.2 Non-functional Requirements Summary

1. iOS + Android
2. Real-time push notifications
3. Secure authentication
4. Payment integration
5. Performance SLA (e.g. key view response times)

---

## 3. Simplified SOW & Effort Estimation

### 3.1 Scope & Effort Summary

| Phase | Hours |
|-------|-------|
| Discovery & Design | 108h |
| Backend Development | 192h |
| Mobile iOS | 140h |
| Mobile Android | 140h |
| QA & Testing | 76h |
| Deployment & Launch | 48h |
| Project Management | 84h |
| **TOTAL** | **788h** |

*SOW covers full project scope — broader than original schedule (562h) due to PM allocation, buffer, and corrected resource plan.*

### 3.2 Timeline
- Total estimated duration: **12-14 weeks**
- Iterative delivery (Agile/Scrum)

### 3.3 Estimated Cost
**Recommendation:** 200,000 – 280,000 PLN net (Mid/Senior team mix)

*Effort estimates based on task-level scope decomposition, comparison with similar projects, and integration risk buffers. This is a preliminary estimate — to be refined after client discovery workshops.*

---

*This is an anonymized document. Company and project names have been removed. All analysis, recommendations, and estimates are original work.*
