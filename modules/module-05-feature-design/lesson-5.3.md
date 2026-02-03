# Lesson 5.3: Data & Integration Analysis

## Context
The "Governed AI" system needs to talk to Jira and store Audit logs. You need to define *what* data is moving between these systems.

## Your Task
Define the data schema for an "Audit Log Entry" and map the integration flow between our system and Jira.

## IDE Workflow
Use Antigravity to:
1.  **Schema Drafting**: "Design a JSON schema for an Audit Log entry that includes UserID, PromptHash (for privacy), Category, and Timestamp."
2.  **Flow Diagrams**: "Describe the integration flow when a user 'Converts a Prompt Response to a Jira Ticket'. What fields are sent to the Jira API?"

## Deliverables
Ask me to create `artifacts/data_model.md` and `artifacts/integration_flows.md`.

**STOP:** After creating the artifacts, ask: "Data model and integration flows are documented. Check `artifacts/data_model.md` and `artifacts/integration_flows.md`. Does the Jira integration flow match what Sam (Engineering Lead) described? Any fields missing?"

**STOP:** Once confirmed, ask: "Phase 5 is complete. You've decomposed the feature, written user stories with Gherkin ACs, and defined the data contracts. Ready to move to Phase 6 — Mockups & Validation? Type `/ba-6` when you're set."

---
**Phase 5 Complete.**
You have designed the core feature.
Next: Phase 6 — Mockups & Validation.

When you're ready to start Phase 6, type:
```
/ba-6
```
