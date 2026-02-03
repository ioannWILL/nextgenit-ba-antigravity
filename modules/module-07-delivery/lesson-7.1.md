<!--
BA Antigravity Course
Copyright (c) 2025 Ivan Vilchavskyi

Licensed under CC BY-NC-ND 4.0
https://creativecommons.org/licenses/by-nc-nd/4.0/

Educational use only. Commercial use and derivatives not permitted.
-->

# Lesson 7.1: Delivery Plan

## Context
Features don't ship all at once. You need a rollout strategy. Phase 1: Internal alpha. Phase 2: Beta for Frontend team. Phase 3: Enterprise release.

## Your Task
Create a Delivery Plan identifying dependencies and the "Release Train" for the MVP.

## IDE Workflow

### Step 1: Why Delivery Planning Matters

**Say:**

"We've designed the feature, validated it with prototypes, and refined the requirements. Now comes the question engineering leads always ask: 'What do we build first?'

Delivery planning isn't just about timelines — it's about:

1. **Dependencies**: You can't build the PII Filter Dashboard without the PII Filter Service
2. **Risk mitigation**: Ship the riskiest parts first so problems surface early
3. **Value delivery**: Get something useful to users quickly, even if incomplete

Jordan mentioned the 'Jan 15 milestone.' That's our constraint. We need to figure out what's realistic to ship by then."

**STOP:** Ask: "Delivery planning forces trade-offs between scope, time, and quality. Have you been in planning sessions where these trade-offs created tension? Let me know when you're ready to map the dependencies."

---

### Step 2: Dependency Mapping

**Say:**

"Let's map what depends on what. Looking at our feature breakdown:

- **Auth & Identity** → Everything depends on this (need users to exist)
- **PII Filter Service** → Depends on Auth (need to know who's submitting)
- **Audit Logging** → Depends on Auth and PII Filter (need events to log)
- **Usage Quotas** → Depends on Auth (need users) and Audit (need to track usage)
- **Jira Integration** → Depends on Auth (need users) and core chat working

This creates a dependency chain. Auth must be done first."

Use Antigravity to:
1. **Dependency Analysis**: "Analyze the feature breakdown in `artifacts/feature_breakdown.md` and create a dependency map. For each epic:
   - List what it depends on (prerequisites)
   - List what depends on it (blockers if delayed)
   - Identify the critical path — the sequence where any delay delays everything

   Format as a Mermaid diagram showing the dependency flow."

**STOP:** After generating the dependency map, ask: "This is the critical path. Notice how Auth is the foundation? If Auth slips, everything slips. This is why senior BAs push for Auth to be prioritized. Does the dependency chain make sense?"

---

### Step 3: Phased Rollout Strategy

**Say:**

"We can't ship everything at once. Let's plan phases:

**Phase 1 — Internal Alpha (Week 1-2)**
- Core: Auth + Basic Chat (no governance yet)
- Audience: 10 internal testers
- Goal: Validate basic flow works

**Phase 2 — Security MVP (Week 3-4)**
- Add: PII Filter + Audit Logging
- Audience: 50 beta users (mix of devs and security)
- Goal: Validate security controls

**Phase 3 — Enterprise Release (Week 5-6)**
- Add: Quotas + Jira Integration + Full RBAC
- Audience: All 500 developers
- Goal: Full production rollout

This is a 'release train' — progressive expansion of scope and audience."

Use Antigravity to:
1. **Rollout Plan**: "Create a phased rollout plan for the Governed AI platform targeting the Jan 15 enterprise release. Include:
   - Phase names and durations
   - Features included in each phase
   - Target audience and size
   - Success criteria for proceeding to next phase
   - Rollback plan if critical issues found

   Reference the feature breakdown and risk register for prioritization."

**STOP:** After generating the rollout plan, ask: "Notice the success criteria — we don't proceed to Phase 2 unless Phase 1 passes. This is risk management in action. Does this phased approach feel realistic for your organization?"

---

### Step 4: Milestone Mapping

**Say:**

"Jordan's exec summary mentioned 'Jan 15 milestone.' Let's map our phases to actual dates and identify what's at risk.

Key questions:
- What's the absolute minimum for Jan 15? (MVP scope)
- What gets cut if we run late? (Scope reduction candidates)
- What's the 'nice to have' vs 'must have'?"

Use Antigravity to:
1. **Milestone Document**: "Create a delivery plan document that includes:
   - Timeline: Map the phases to calendar dates working back from Jan 15
   - MVP Scope: The minimum feature set for Jan 15 (must-haves)
   - Stretch Goals: Features that ship if time permits (nice-to-haves)
   - Risk Buffer: What happens if we lose a week to bugs?
   - Go/No-Go Criteria: How we decide if we're ready for enterprise release

   This becomes the document the steering committee reviews."

---

## Deliverables
Ask me to create `artifacts/delivery_plan.md` with phases, dependencies, and timeline.

**STOP:** After creating the artifact, ask: "Delivery plan is ready. Open `artifacts/delivery_plan.md` and review:
- Does the phased rollout make sense?
- Are the MVP vs stretch goal distinctions clear?
- Does this timeline align with the Jan 15 milestone from the exec summary?

This is what you'd present to Jordan and the steering committee. Ready for Jira integration in Lesson 7.2?"

---
Move to Lesson 7.2.
