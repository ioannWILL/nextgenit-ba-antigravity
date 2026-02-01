# Lesson 3.3: Jira vs Code vs Discovery Gap

## Context
You have interview notes (Needs), a Jira backlog (Planned work), and the real OpenClaw repository (Reality). A senior BA finds the "truth" in the intersection of these three.

## Your Task
Conduct a Gap Analysis. What is being planned in Jira that isn't supported by the code? What did stakeholders ask for that isn't in either? Where does the real codebase contradict the executive's assumptions?

## IDE Workflow

### Step 1: Three-Source Cross-Reference

**Say:**

"Now we have all three sources of truth loaded in one workspace. This is where Antigravity earns its keep — cross-referencing multiple files simultaneously."

Use Antigravity to:
1. **Cross-Reference**: "Compare the `discovery-results/jira_existing.md` backlog with the capabilities you documented in `artifacts/as_is_capabilities.md` (based on the real OpenClaw repo). Which Jira tickets are currently technically impossible without a complete rewrite? Which ones are partially addressed by the existing codebase?"
2. **Missing Requirements**: "Are there any 'Security' requirements from Alex (CISO) in `artifacts/stakeholder_needs.md` that don't have a corresponding Jira ticket yet? List them with severity."

---

### Step 2: Architecture-Aware Gap Identification

**Say:**

"Now let's use the architecture diagrams from Lesson 3.2 to identify structural gaps."

Use Antigravity to:
1. **Structural Gaps**: "Based on the As-Is vs To-Be diagram in `artifacts/as_is_feature_map.md`, list every new component that needs to be built from scratch vs components that can extend existing code in `openclaw-repo/`. Estimate the relative complexity (Low/Medium/High) for each."
2. **Dependency Chain**: "Which new components depend on other new components? For example, can we build the Usage Dashboard without first building Per-User Quotas? Map the dependencies."

---

## Deliverables
Create `artifacts/gap_analysis.md` summarizing the Delta, including:
- A table: [Stakeholder Need] → [Jira Status] → [Code Reality] → [Gap Type]
- A list of structurally missing components with complexity estimates
- A dependency chain for new components

**STOP:** Verify the student has created `artifacts/gap_analysis.md` before proceeding.

---
**Phase 3 Complete.**
You now know exactly where the prototype fails and what needs to be built from scratch — based on the real codebase, not assumptions.
Next: Phase 4 — Requirements Analysis.

When you're ready to start Phase 4, type:
```
/ba-4
```
