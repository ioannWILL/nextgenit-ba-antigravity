# Lesson 3.2: Architecture Diagrams & Business Feature Mapping

## Context
Stakeholders don't understand `import openai` or module structures. They understand "Code Generation" and "Safety Filtering." You need to translate the real technical architecture into business-facing features — and create visual diagrams that anyone can read.

## Your Task
Analyze the cloned OpenClaw repository and create architecture diagrams (using Mermaid) that map the "As-Is" state. Then translate technical components into a business feature map.

## IDE Workflow

### Step 1: High-Level Architecture Diagram

**Say:**

"Let's create a visual representation of how the system works today. This is something you'd put in front of the CTO or a steering committee."

Use Antigravity to:
1. **Architecture Diagram**: "Based on the `openclaw-repo/` codebase, generate a Mermaid architecture diagram showing the main components and how they interact: user input flow, LLM API calls, response handling, file system interactions, and any integrations. Use `graph TD` (top-down) format."

**Check:** Review the generated diagram. Ask the student: "Does this match what you expected from the interviews? Where are the governance components?"

---

### Step 2: Request Flow Diagram

**Say:**

"Now let's trace a single request through the system — from a developer typing a prompt to getting a response."

Use Antigravity to:
1. **Sequence Diagram**: "Generate a Mermaid sequence diagram showing the lifecycle of a single user prompt through the OpenClaw codebase. Include every step: input parsing, any middleware/filtering, API call, response processing, and output. Highlight where **PII risk** exists (data that passes unfiltered to external APIs)."

---

### Step 3: Business Feature Translation

**Say:**

"Diagrams are great for architects. But the business side needs a different view — what does this system *do* in their language?"

Use Antigravity to:
1. **Feature Map Table**: "Based on the repository analysis, create a table with three columns: [Technical Component/Module] → [Business Feature Name] → [Current Limitation]. For example: `openai.ChatCompletion.create` → 'AI Code Generation' → 'No rate limiting, shared API key'."
2. **Glossary**: "Create a glossary of technical terms from the OpenClaw codebase for non-technical stakeholders. Include terms they'll hear in meetings: API, token, prompt, embedding, rate limit, etc."

---

### Step 4: Gap Visualization — As-Is vs To-Be

**Say:**

"One more diagram. This is the one that sells the project. Show the current state next to the target state."

Use Antigravity to:
1. **As-Is vs To-Be**: "Generate a Mermaid diagram showing the current OpenClaw architecture on the left and the target 'Governed AI Platform' architecture on the right. The target should include: RBAC layer, PII scrubbing middleware, audit logging service, usage quota manager, and SSO integration. Use different colors or styles to distinguish existing vs new components."

---

## Deliverables
Ask me to create `artifacts/as_is_feature_map.md` with:
- A high-level architecture diagram (Mermaid).
- A request flow sequence diagram (Mermaid).
- An As-Is vs To-Be comparison diagram (Mermaid).
- A table: [Tech Component] → [Business Feature] → [Current Limitation].
- A glossary for non-technical stakeholders.

---
**STOP:** Verify the artifacts are created with all diagrams, then move to Lesson 3.3.
