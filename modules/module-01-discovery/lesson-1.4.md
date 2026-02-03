# Lesson 1.4: Discovery Backlog

## Context
Usually, BAs rush to write requirements. A *senior* BA knows that more discovery is needed when information is contradictory. You need to identify what we *don't* know yet.

## Your Task
Create a backlog of "Discovery Tasks" (spikes, research items, follow-up meetings) required to reduce the project's ambiguity.

## IDE Workflow

### Step 1: Why Discovery Backlogs Matter

**Say:**

"We've synthesized interviews, compared executive vision to reality, and identified gaps. But here's what separates senior BAs from junior ones:

**Knowing what you don't know.**

We've made assumptions. We've identified risks. But we haven't verified them. A discovery backlog is a list of 'things we need to find out before we can write confident requirements.'

Types of discovery tasks:
- **Spikes**: Technical investigations ('Can the existing auth system support RBAC?')
- **Follow-up meetings**: Stakeholder clarifications ('Alex mentioned PII concerns — what specific data types?')
- **Research**: External information ('What are industry standards for AI governance?')
- **Proof of concepts**: Validation ('Build a prototype PII filter to test latency impact')

These aren't features. They're investments in reducing uncertainty."

**STOP:** Ask: "Discovery backlogs are often skipped because they 'don't feel like progress.' But they prevent expensive mistakes later. Have you seen projects fail because assumptions weren't validated? Let me know when you're ready to identify our unknowns."

---

### Step 2: Identifying Technical Unknowns

**Say:**

"Let's start with what we don't know technically. The security interview mentioned 'PII scrubbing' — but do we actually know how to implement that?"

Use Antigravity to:
1. **Technical Unknowns**: "Based on the security interview in `discovery-results/interviews/` and the exec summary, list the technical unknowns that need investigation before we can write requirements. For each unknown:
   - What we don't know
   - Why it matters (risk if we guess wrong)
   - How to find out (spike, POC, research)
   - Who needs to be involved"

**STOP:** After identifying unknowns, ask: "Each of these unknowns is a potential project blocker. If we write requirements assuming we can 'just add PII filtering' without knowing the latency impact, we might promise something impossible."

---

### Step 3: Identifying Stakeholder Unknowns

**Say:**

"Technical unknowns are one category. Stakeholder unknowns are another — things we need to clarify with people."

Use Antigravity to:
1. **Stakeholder Unknowns**: "Review the gaps identified in `artifacts/exec_vs_delivery_gap.md` and `artifacts/questions_for_exec.md`. Convert these into discovery tasks:
   - What decision needs to be made
   - Who can make it
   - What information they need to decide
   - Suggested meeting format (1:1, workshop, email)"

---

### Step 4: Prioritizing the Backlog

**Say:**

"Not all unknowns are equal. Some block everything (can't start without this). Others are nice-to-know (affects later phases).

Let's prioritize using blocking impact:
- **Critical**: Blocks Phase 4 (Requirements Analysis) — must resolve first
- **High**: Blocks later phases — resolve soon
- **Medium**: Affects quality but not blocking — resolve when time permits"

Use Antigravity to:
1. **Backlog Prioritization**: "Compile all discovery tasks into a prioritized backlog. For each task:
   - Task description
   - Type (Spike / Meeting / Research / POC)
   - Priority (Critical / High / Medium)
   - Owner (who should do this)
   - Definition of Done (how we know it's resolved)
   - Stakeholder (who needs the answer)"

---

### Step 5: Optional Jira Integration

**Say:**

"In a real project, these discovery tasks should be tracked in Jira — not just in a Markdown file. If you have Jira connected, I can create these as tickets.

Discovery tasks in Jira typically use:
- **Issue Type**: Task or Spike (if your project has spike type)
- **Labels**: discovery, investigation
- **Epic Link**: 'Phase 0 - Discovery' or similar

This makes discovery visible to the team — it's real work, not 'pre-work.'"

---

## Deliverables
Ask me to create `artifacts/discovery_backlog.md` with a prioritized list of tasks including:
- Task description
- Type (Spike / Meeting / Research / POC)
- Priority (Critical / High / Medium)
- Owner suggestion
- Definition of Done
- Stakeholder who needs the answer

**STOP:** After creating the artifact, ask: "Review `artifacts/discovery_backlog.md`. Is anything missing? Any unknowns we haven't captured? This backlog represents the 'homework' before we can write confident requirements."

**STOP (Optional):** Ask: "Would you like me to create these as Jira issues in your connected project? I can create them as Tasks or Spikes with appropriate labels."

**STOP:** Once confirmed, ask: "Phase 1 is complete. You've moved from messy interviews to:
- Structured stakeholder needs
- Executive-reality gap analysis
- Questions for leadership
- A prioritized discovery backlog

This is professional-grade discovery. Ready to move to Phase 2 — Problem Framing? Type `/ba-2` when you're set."

---
**Phase 1 Complete.**
You have moved from messy interviews to a structured discovery plan.
Next: Phase 2 — Problem Framing.

When you're ready to start Phase 2, type:
```
/ba-2
```
