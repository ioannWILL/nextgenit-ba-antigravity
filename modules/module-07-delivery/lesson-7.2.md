# Lesson 7.2: Push to Jira via MCP

## Context
A BA's job isn't done until the tickets are in the system. Instead of manual entry, you will use Antigravity's MCP (Model Context Protocol) to sync your local Markdown files with Jira.

## Your Task
Formulate the prompts to have Antigravity create the Epic and Stories you've designed directly in your Jira project.

## IDE Workflow

### Option A: Live Jira Integration (if Atlassian MCP is connected)

Use Antigravity to:
1.  **Jira Sync**: "Using the `atlassian-mcp-server`, create an Epic in Jira titled 'Governed AI MVP' and populate it with 3 stories from `artifacts/user_stories.md`."
2.  **Linking**: "Link the local artifacts (like `artifacts/functional_requirements.md`) to the Jira tickets as comments or remote links."

### Option B: Simulation Fallback (if Atlassian MCP is NOT available)

**Say:**

"If you don't have Jira connected, we'll simulate the output locally. The exercise is the same — you're defining what goes into the delivery pipeline."

Use Antigravity to:
1.  **Simulated Jira Export**: "Based on `artifacts/user_stories.md` and `artifacts/delivery_plan.md`, ask me to create `artifacts/jira_simulation.md` containing the Epic, 3 Stories, and their Acceptance Criteria formatted as Jira tickets would appear (Key, Summary, Description, AC, Priority, Labels)."
2.  **Linking Simulation**: "Ask me to add a section to `artifacts/jira_simulation.md` listing which local artifacts would be linked to each ticket as remote links."

## Deliverables
- **If MCP connected:** Evidence of Jira ticket creation (summaries and keys created by Antigravity).
- **If simulated:** `artifacts/jira_simulation.md` with formatted ticket output.

**STOP:** Verify the deliverables are created before wrapping Phase 7.

---
**Phase 7 Complete.**
The project is now live in the development pipeline.
Next: Phase 8 — Validation & Executive Readout.

When you're ready to start Phase 8, type:
```
/ba-8
```
