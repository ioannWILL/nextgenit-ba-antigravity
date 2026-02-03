# Lesson 2.2: Define Scope & Out-of-Scope

## Context
The scope is leaking. The frontend team wants a React UI, the backend team wants a CLI, and the CTO wants Java/Go support. If we try to do everything by Jan 15, we will fail.

## Your Task
Be the "Scope Guardian." Use the MoSCoW method (Must have, Should have, Could have, Won't have) to define the MVP.

## IDE Workflow

### Step 1: The Scope Guardian Role

**Say:**

"Here's a truth about projects: everyone wants their feature to be 'in scope.' The frontend team wants a beautiful React UI. The backend team wants a powerful CLI. Security wants enterprise SSO. The CTO wants it all by Jan 15.

Your job as the BA is to be the 'Scope Guardian' — the person who protects the project from trying to do everything and failing at all of it.

Scope creep is the #1 project killer. It's not that people have bad ideas — they have too many good ideas for the timeline. The BA draws the line and makes it visible."

**STOP:** Ask: "Have you been on projects where scope crept until the deadline became impossible? Being the 'Scope Guardian' requires saying 'no' — or at least 'not yet.' Let me know when you're ready to prioritize."

---

### Step 2: Understanding MoSCoW

**Say:**

"We'll use the MoSCoW method for prioritization. It's simple but powerful:

- **Must have**: Without these, the project fails. Jan 15 is meaningless without them.
- **Should have**: Important, but we could launch without them if pushed. Adds significant value.
- **Could have**: Nice to have. We'll add them if time permits. Won't break the launch if missing.
- **Won't have (this time)**: Explicitly out of scope for this release. Future consideration.

The magic is in 'Won't have.' By explicitly listing what we're NOT doing, we prevent the 'oh, I thought that was included' surprise."

**STOP:** Ask: "The 'Won't have' category is uncomfortable because it means saying 'no' to someone. But it's the most important category — it sets expectations. Ready to categorize our features?"

---

### Step 3: Prioritizing for Jan 15

**Say:**

"Let's look at everything stakeholders have requested and apply the Jan 15 deadline filter.

Questions to ask:
- Can we launch without this? → If yes, it's not 'Must have'
- Does Security require this? → Probably 'Must have' (can't launch non-compliant)
- Does it affect the 500-developer rollout? → 'Should have' at minimum
- Is it one team's preference? → Probably 'Could have'"

Use Antigravity to:
1. **MoSCoW Prioritization**: "Based on `artifacts/stakeholder_needs.md`, `artifacts/exec_vs_delivery_gap.md`, and the Jan 15 deadline, create a MoSCoW table for the Governed AI MVP. For each item:
   - Feature/Requirement
   - MoSCoW Category (Must/Should/Could/Won't)
   - Rationale (why this category?)
   - Stakeholder (who requested it?)

   Be strict with 'Must have' — only include things that would cause launch failure if missing."

**STOP:** After the MoSCoW table, ask: "Look at the 'Must have' list. Is it achievable by Jan 15? If it looks too big, we need to be more ruthless. The goal is a realistic MVP, not a wish list."

---

### Step 4: Defending 'Won't Have' Decisions

**Say:**

"Now the hard conversation: explaining why things are 'Won't have.'

Jenny requested dark mode. Sam wants Go/Java support. The mobile team wants a mobile app. All valid requests — but not for Jan 15.

Each 'Won't have' needs a rationale that a stakeholder can understand (even if they disagree)."

Use Antigravity to:
1. **Trade-off Documentation**: "For each 'Won't have' item, write a brief explanation suitable for stakeholder communication:
   - What was requested
   - Why it's not in MVP (timeline, dependencies, complexity)
   - When it might be considered (Phase 2, Q2, etc.)
   - Alternative or workaround if any

   Example: 'Dark Mode: Requested by Jenny (Frontend). Not in MVP because UI polish is lower priority than security compliance. Planned for Phase 2 (Feb). Workaround: OS-level dark mode works with our neutral color scheme.'"

**STOP:** After trade-off documentation, ask: "These explanations are for stakeholder communication. Do they feel respectful of the requests while being clear about the decision? Anyone you think would push back hard?"

---

### Step 5: The Scope Document

**Say:**

"Finally, we create the formal scope document. This becomes the reference for all 'is this in scope?' questions.

Two artifacts:
1. **Scope Definition**: What we ARE building (MoSCoW table)
2. **Out of Scope**: What we are NOT building (explicit list with rationale)

Both are equally important. The 'Out of Scope' document prevents arguments later."

Use Antigravity to:
1. **Scope Finalization**: "Create the final scope artifacts with:
   - MoSCoW table (all categories)
   - Out of scope list with rationale and future timeline
   - Scope change process (how to request changes)
   - Approval line (who signs off on scope)"

---

## Deliverables
Ask me to create `artifacts/scope_definition.md` with a MoSCoW table showing all features categorized by priority.
Ask me to create `artifacts/out_of_scope.md` explicitly listing items we are NOT building yet, with rationale and future timeline.

**STOP:** After creating the artifacts, ask: "Review both artifacts:
- `artifacts/scope_definition.md`: Is the 'Must have' list realistic for Jan 15?
- `artifacts/out_of_scope.md`: Would stakeholders understand why their requests are deferred?

Optionally, would you like me to create Confluence pages from these for team visibility?"

**STOP:** Once confirmed, ask: "Scope is defined. You now have a clear 'in' and 'out' list that protects the project from creep. Ready for Lesson 2.3 where we'll create a branded presentation for stakeholder alignment?"

---
Move to Lesson 2.3.
