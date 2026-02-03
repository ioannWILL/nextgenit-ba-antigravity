# Lesson 5.3: Data & Integration Analysis

## Context
The "Governed AI" system needs to talk to Jira and store Audit logs. You need to define *what* data is moving between these systems.

## Your Task
Define the data schema for an "Audit Log Entry" and map the integration flow between our system and Jira.

## IDE Workflow

### Step 1: Why Data Contracts Matter

**Say:**

"We've defined what the system does (requirements) and how to build it (stories). Now we need to define what data flows through it. This is critical because:

1. **Engineers need schemas**: They can't build a database without knowing what fields to store
2. **Integrations need contracts**: Jira won't accept random data — we need to map our fields to their API
3. **Security needs visibility**: Alex wants to audit what data leaves the system

A data model is the 'source of truth' that prevents the classic problem: 'The frontend sends field X, but the backend expects field Y.'"

**STOP:** Ask: "Data contracts prevent integration failures. Have you seen projects where mismatched data formats caused bugs? Let me know when you're ready to design the audit log schema."

---

### Step 2: Audit Log Schema Design

**Say:**

"The audit log is central to Alex's security requirements. Every prompt, every response, every override needs to be logged. But we need to be careful:

- **What to log**: User, timestamp, action, result
- **What NOT to log**: The actual prompt content (PII risk!)
- **Privacy technique**: Log a hash of the prompt, not the prompt itself

This is a classic trade-off: Alex wants full visibility, but logging raw prompts creates the exact PII risk we're trying to prevent."

Use Antigravity to:
1. **Schema Design**: "Design a JSON schema for an Audit Log entry that balances security visibility with privacy. Include:
   - `event_id`: Unique identifier
   - `timestamp`: ISO 8601 format
   - `user_id`: Who performed the action
   - `user_role`: Their RBAC role at time of action
   - `action_type`: What they did (PROMPT_SUBMITTED, PII_DETECTED, OVERRIDE_REQUESTED, etc.)
   - `prompt_hash`: SHA-256 hash of prompt (for correlation, not content)
   - `pii_detected`: Boolean
   - `outcome`: SUCCESS, BLOCKED, OVERRIDE_APPROVED
   - `metadata`: Flexible object for action-specific data

   Explain why each field exists and what privacy considerations apply."

**STOP:** After generating the schema, ask: "Notice we're logging the prompt *hash*, not the prompt itself. This lets security correlate events without storing sensitive content. Does this balance make sense? Any fields missing for compliance?"

---

### Step 3: Jira Integration Flow

**Say:**

"Sam's team wants to convert AI responses into Jira tickets. This means our system needs to talk to Jira's API. We need to map:

- What triggers the integration (user clicks 'Create Ticket')
- What data we send (summary, description, labels)
- What we get back (ticket key, URL)
- What we store (link between prompt and ticket)

This is integration design — defining the contract between two systems."

Use Antigravity to:
1. **Integration Flow**: "Design the integration flow for 'Convert AI Response to Jira Ticket'. Document:

   **Trigger**: User clicks 'Create Jira Ticket' on an AI response

   **Data Mapping**:
   | Our Field | Jira Field | Notes |
   |-----------|------------|-------|
   | response_summary | Summary | First 100 chars of AI response |
   | ... | ... | ... |

   **API Call**: POST to `/rest/api/3/issue`

   **Response Handling**: Store ticket key, display link to user

   **Error Handling**: What if Jira is down? What if user lacks Jira access?

   Reference the Jira REST API documentation for field names."

**STOP:** After generating the flow, ask: "This is the Jira integration contract. Notice we're handling error cases — what happens when Jira is unavailable? Sam's team will need this for implementation. Does the data mapping look complete?"

---

### Step 4: Data Flow Diagram

**Say:**

"Let's visualize all the data flows in the system. This diagram shows what data moves where — essential for security reviews and architecture discussions."

Use Antigravity to:
1. **Data Flow Diagram**: "Create a Mermaid diagram showing data flows in the Governed AI platform:
   - User input → PII Filter → LLM API
   - LLM Response → Response Handler → User
   - All actions → Audit Log Service → Audit Database
   - User action → Jira Integration → Jira API

   Highlight where sensitive data exists and where it's sanitized."

---

## Deliverables
Ask me to create `artifacts/data_model.md` with the audit log schema and field explanations.
Ask me to create `artifacts/integration_flows.md` with the Jira integration design and data flow diagram.

**STOP:** After creating the artifacts, ask: "Data model and integration flows are documented. Review:
- `artifacts/data_model.md`: Does the audit schema capture what Alex needs without storing PII?
- `artifacts/integration_flows.md`: Does the Jira flow match what Sam described? Any edge cases missing?

These documents become the technical contract between BA and engineering."

**STOP:** Once confirmed, ask: "Phase 5 is complete. You've produced the core design artifacts:
- **Feature Breakdown**: Epics, stories, and tasks for sprint planning
- **User Stories**: Detailed stories with Gherkin acceptance criteria
- **Data Model**: Schemas for audit logging with privacy considerations
- **Integration Flows**: Jira API contract and data flow diagrams

Ready to move to Phase 6 — Mockups & Validation? Type `/ba-6` when you're set."

---
**Phase 5 Complete.**
You have designed the core feature.
Next: Phase 6 — Mockups & Validation.

When you're ready to start Phase 6, type:
```
/ba-6
```
