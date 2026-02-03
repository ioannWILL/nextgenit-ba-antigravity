<!--
BA Antigravity Course
Copyright (c) 2025 Ivan Vilchavskyi

Licensed under CC BY-NC-ND 4.0
https://creativecommons.org/licenses/by-nc-nd/4.0/

Educational use only. Commercial use and derivatives not permitted.
-->

# Lesson 7.2: Push to Jira via MCP

## Context
A BA's job isn't done until the tickets are in the system. Instead of manual entry, you will use Antigravity's MCP (Model Context Protocol) to sync your local Markdown files with Jira.

## Your Task
Formulate the prompts to have Antigravity create the Epic and Stories you've designed directly in your Jira project.

## IDE Workflow

### Step 1: Why Jira Integration Matters

**Say:**

"You've created beautiful artifacts: requirements, user stories, feature breakdowns. But here's the reality:

- Engineers don't read Markdown files in a repo
- They read Jira tickets in their sprint board
- If it's not in Jira, it doesn't get built

A senior BA bridges this gap. The artifacts are the 'source of truth,' but Jira is 'where work happens.' We need to sync them."

**STOP:** Ask: "The 'documentation vs ticketing' gap is real in every organization. Have you experienced disconnects where requirements existed but weren't in the backlog? Let me know when you're ready to create the Jira structure."

---

### Step 2: Epic and Story Structure

**Say:**

"Before we push to Jira, let's define the structure:

**Epic**: Governed AI MVP
- Contains all stories for the Jan 15 release
- Links to `artifacts/functional_requirements.md` as background

**Stories** (from our user stories document):
- Each story becomes a Jira ticket
- Acceptance criteria become the 'Definition of Done'
- Links to the feature file (`.feature`) for Gherkin scenarios

**Labels and Components**:
- Security, Auth, PII, Quotas, Integration
- Priority: Critical, High, Medium, Low

This hierarchy maps to how Sam's engineering team will plan sprints."

---

### Option A: Live Jira Integration (if Atlassian MCP is connected)

**Say:**

"If you have the Atlassian MCP server connected, we can create tickets directly. This is the power of MCP — your IDE talks to Jira's API."

Use Antigravity to:
1. **Epic Creation**: "Using the Atlassian MCP server, create an Epic in Jira:
   - Summary: 'Governed AI MVP'
   - Description: Link to requirements and delivery plan
   - Labels: governed-ai, mvp, security"

2. **Story Creation**: "Create 3 priority stories under the Epic from `artifacts/user_stories.md`:
   - The SSO Authentication story
   - The PII Filter story
   - The Audit Logging story

   For each, include the Gherkin acceptance criteria in the description."

3. **Linking**: "Add remote links to each Jira ticket pointing to the relevant local artifacts (functional requirements, user stories, etc.)"

**STOP:** After Jira tickets are created, ask: "The tickets are live in Jira. Check your Jira board — you should see the Epic and Stories. Does the structure match how your team organizes work?"

---

### Option B: Simulation Fallback (if Atlassian MCP is NOT available)

**Say:**

"If you don't have Jira connected, we'll simulate the output locally. The exercise is the same — you're defining exactly what goes into Jira. In a real project, you'd copy-paste or use Jira's CSV import."

Use Antigravity to:
1. **Simulated Epic**: "Create a simulated Jira export showing the Epic structure:
   - Key: GOVAI-1
   - Type: Epic
   - Summary: Governed AI MVP
   - Description: [Full description with links to artifacts]
   - Labels: governed-ai, mvp
   - Status: To Do"

2. **Simulated Stories**: "Create 3 simulated Jira stories based on `artifacts/user_stories.md`:
   - Key: GOVAI-2, GOVAI-3, GOVAI-4
   - Epic Link: GOVAI-1
   - Include: Summary, Description, Acceptance Criteria, Priority, Labels
   - Format exactly as Jira tickets would appear"

3. **Artifact Links**: "Add a section showing which artifacts link to which tickets:
   | Ticket | Linked Artifacts |
   |--------|-----------------|
   | GOVAI-1 | functional_requirements.md, delivery_plan.md |
   | GOVAI-2 | user_stories.md (SSO section), login_flow.feature |
   | ... | ... |"

**STOP:** After simulation, ask: "This is exactly what would go into Jira. Review `artifacts/jira_simulation.md`:
- Does each ticket have enough detail for an engineer to start work?
- Are the acceptance criteria specific enough?
- Would Sam's team be able to estimate these stories?"

---

### Step 3: Traceability Matrix

**Say:**

"One last artifact: a traceability matrix. This shows the chain from stakeholder need → requirement → story → ticket.

Why it matters:
- When Jordan asks 'Did we address the security concerns?' you can trace to specific tickets
- When QA asks 'What requirement does this ticket fulfill?' the answer is clear
- When audit asks 'Why did we build this?' there's a paper trail"

Use Antigravity to:
1. **Traceability Matrix**: "Create a traceability matrix showing:
   | Stakeholder Need | Requirement ID | User Story | Jira Ticket |
   |-----------------|----------------|------------|-------------|
   | Alex: PII Protection | FR-003 | PII Filter Story | GOVAI-3 |
   | Sam: Jira Integration | FR-007 | Jira Ticket Story | GOVAI-5 |
   | ... | ... | ... | ... |

   This becomes an appendix to the delivery plan."

---

## Deliverables
- **If MCP connected:** Evidence of Jira ticket creation (summaries and keys created by Antigravity).
- **If simulated:** `artifacts/jira_simulation.md` with formatted ticket output and traceability matrix.

**STOP:** After creating the deliverables, ask: "Jira structure is defined (live or simulated). Review the tickets:
- Is each ticket self-contained enough for an engineer to work independently?
- Do the acceptance criteria match the Gherkin scenarios from Phase 5?
- Can you trace every ticket back to a stakeholder need?

This is the handoff point — artifacts become backlog items."

**STOP:** Once confirmed, ask: "Phase 7 is complete. You've bridged documentation and delivery:
- **Delivery Plan**: Phased rollout with dependencies and milestones
- **Jira Structure**: Epic and stories ready for sprint planning
- **Traceability**: Every ticket traces to requirements and stakeholder needs

The project is now in the engineering pipeline. Ready to move to Phase 8 — Validation & Executive Readout? Type `/ba-8` when you're set."

---
**Phase 7 Complete.**
The project is now live in the development pipeline.
Next: Phase 8 — Validation & Executive Readout.

When you're ready to start Phase 8, type:
```
/ba-8
```
