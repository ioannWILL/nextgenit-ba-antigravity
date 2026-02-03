<!--
BA Antigravity Course
Copyright (c) 2025 Ivan Vilchavskyi

Licensed under CC BY-NC-ND 4.0
https://creativecommons.org/licenses/by-nc-nd/4.0/

Educational use only. Commercial use and derivatives not permitted.
-->

# Lesson 6.3: UX Review & Iteration

## Context
Usually, once a BA sees the prototype, they realize some requirements were wrong. "Actually, users should be able to override the PII filter if it's a false positive."

## Your Task
Conduct a "Self-Review" of your requirements based on the prototype. Identify 3 friction points.

## IDE Workflow

### Step 1: The Iteration Mindset

**Say:**

"Here's the uncomfortable truth about BA work: your first requirements are almost never right. That's not failure — that's the process.

Prototypes exist to find problems early. It's much cheaper to discover 'this flow is annoying' now than after 3 sprints of development.

The key questions:
- What feels clunky when you actually use it?
- What did we assume that turned out to be wrong?
- What edge cases did we miss?

This is called *requirements iteration* — updating our artifacts based on validation."

**STOP:** Ask: "Iteration is a sign of good BA work, not bad planning. Have you had experiences where early prototypes changed your understanding of requirements? Let me know when you're ready to critique our own work."

---

### Step 2: Identifying Friction Points

**Say:**

"Let's be critical of the prototype we just built. Think like a frustrated developer at 6 PM trying to ship a feature:

1. **PII Warning Friction**: The warning blocks everything. What if I'm in a hurry and it's a false positive?
2. **Override Flow**: I have to wait for Security approval? That could take hours!
3. **No Feedback**: After I edit my prompt, how do I know it's now 'clean'?

Each of these is a UX friction point that could make developers hate the system — which defeats the adoption goal."

Use Antigravity to:
1. **Friction Analysis**: "Based on the prototype in `artifacts/local_prototype.html`, identify 3-5 UX friction points for developers using the Governed AI platform. For each:
   - Describe the friction
   - Explain the user's frustration
   - Propose a solution
   - Note if this requires a requirement change

   Consider: workflow interruptions, waiting times, unclear feedback, missing escape hatches."

**STOP:** After the analysis, ask: "These friction points are real problems. Notice how 'security' and 'usability' conflict? Alex wants everything blocked, developers want to work fast. This is the trade-off BAs navigate. Which friction points concern you most?"

---

### Step 3: Updating Requirements

**Say:**

"Now we update our artifacts. This is the iteration loop:

1. Prototype revealed friction →
2. We identify root cause →
3. We update requirements/stories →
4. Engineers build updated flow

Let's add a new user story for the 'Override with self-approval for false positives' flow. This addresses friction while maintaining audit trail."

Use Antigravity to:
1. **Story Update**: "Add a new user story to handle the 'false positive override' scenario:
   - Story: As a developer, I want to self-approve an override when the PII filter flags a false positive, so that I can continue working without waiting for Security approval.
   - Include Gherkin acceptance criteria
   - Include the constraint: 'All self-approvals are logged and reviewed weekly by Security'

   This balances usability (fast override) with security (audit trail)."

**STOP:** After the story update, ask: "This new story addresses the friction without removing security controls. Notice the constraint about logging — that's how we satisfy both developers AND Alex. Does this balance feel right?"

---

### Step 4: Documenting UX Feedback

**Say:**

"Let's capture all the UX feedback formally. This document serves two purposes:

1. **Decision log**: Why did we change the requirements?
2. **Backlog input**: Some friction points might become future enhancements

Not every friction point gets fixed in MVP. Some get deferred to v2."

Use Antigravity to:
1. **UX Feedback Document**: "Create a UX feedback document that captures:
   - Friction points identified (from Step 2)
   - Resolution for each: Fixed in MVP / Deferred to v2 / Won't fix (with reason)
   - Requirement changes made
   - Open questions for stakeholders

   Format as a professional document suitable for a steering committee review."

---

## Deliverables
Ask me to create `artifacts/ux_feedback.md` with friction points and resolutions.
Ask me to update `artifacts/user_stories.md` with the new override flow story.

**STOP:** After creating/updating the artifacts, ask: "UX feedback captured and user stories updated. Review:
- `artifacts/ux_feedback.md`: Do these friction points match what you observed testing the prototype?
- `artifacts/user_stories.md`: Check the new self-approval override story — does it balance security and usability?

This iteration loop — prototype → feedback → update — is how mature BA teams work."

**STOP:** Once confirmed, ask: "Phase 6 is complete. You've validated the design through:
- **Wireframes**: Layout and RBAC-based UI
- **Interactive Prototype**: PII filter flow stakeholders can test
- **UX Feedback**: Friction points identified and addressed
- **Updated Stories**: Requirements refined based on validation

This is 'shift-left' testing — finding problems before code is written. Ready to move to Phase 7 — Delivery & Atlassian Integration? Type `/ba-7` when you're set."

---
**Phase 6 Complete.**
You have a validated design.
Next: Phase 7 — Delivery & Atlassian Integration.

When you're ready to start Phase 7, type:
```
/ba-7
```
