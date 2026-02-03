<!--
BA Antigravity Course
Copyright (c) 2025 Ivan Vilchavskyi

Licensed under CC BY-NC-ND 4.0
https://creativecommons.org/licenses/by-nc-nd/4.0/

Educational use only. Commercial use and derivatives not permitted.
-->

# Lesson 3.2: Architecture Diagrams & Business Feature Mapping

## Context
Stakeholders don't understand `import openai` or module structures. They understand "Code Generation" and "Safety Filtering." You need to translate the real technical architecture into business-facing features — and create visual diagrams that anyone can read.

## Your Task
Analyze the cloned OpenClaw repository and create architecture diagrams (using Mermaid) that map the "As-Is" state. Then translate technical components into a business feature map.

## Viewing Mermaid Diagrams

**Say:**

"Before we create the diagrams, let's make sure you can view them. Mermaid is a 'Documentation as Code' tool — you write diagrams in plain text, and they render visually. To see the diagrams in VS Code, you'll need an extension."

**ACTION:** Guide the student to install the extension:
1. Open the Extensions panel (Cmd+Shift+X on Mac, Ctrl+Shift+X on Windows)
2. Search for `Markdown Preview Mermaid Support`
3. Install the extension by `Matt Bierner`
4. After installation, open any `.md` file and use `Cmd+Shift+V` (Mac) or `Ctrl+Shift+V` (Windows) to preview — Mermaid diagrams will now render

**Say:**

"Once installed, you can preview any Markdown file with Mermaid blocks. The diagrams render live as you edit."

**Pro Tip — Enterprise Documentation:**

"In enterprise environments, Mermaid diagrams are portable:
- **Confluence**: If your company has the Mermaid plugin installed, you can paste these diagram blocks directly into Confluence pages — they'll render natively. Check with your wiki admin.
- **GitHub/GitLab**: Both render Mermaid in Markdown files automatically.
- **Alternative tools**: If your team prefers other 'Docs as Code' tools, the same concepts apply to **PlantUML** (more verbose but powerful for sequence diagrams) or **Draw.io** (visual editor with export options). The skill is the same — translating architecture into shareable diagrams."

**STOP:** Ask: "Is the Mermaid preview extension installed? Try opening a Markdown file and previewing it. Let me know when you're ready to create the architecture diagrams."

---

## IDE Workflow

### Step 1: High-Level Architecture Diagram

**Say:**

"Let's create a visual representation of how the system works today. This is something you'd put in front of the CTO or a steering committee."

Use Antigravity to:
1. **Architecture Diagram**: "Based on the `course-repo/` codebase, generate a Mermaid architecture diagram showing the main components and how they interact: user input flow, LLM API calls, response handling, file system interactions, and any integrations. Use `graph TD` (top-down) format."

**STOP:** After generating the diagram, ask: "Here's the architecture diagram. Does this match what you expected from the interviews? Notice anything missing — like governance components? Let me know your thoughts before we move on."

---

### Step 2: Request Flow Diagram

**Say:**

"Now let's trace a single request through the system — from a developer typing a prompt to getting a response."

Use Antigravity to:
1. **Sequence Diagram**: "Generate a Mermaid sequence diagram showing the lifecycle of a single user prompt through the OpenClaw codebase. Include every step: input parsing, any middleware/filtering, API call, response processing, and output. Highlight where **PII risk** exists (data that passes unfiltered to external APIs)."

**STOP:** After generating the sequence diagram, ask: "This shows the request flow with PII risk points highlighted. Can you see where unfiltered data goes to external APIs? Ready for the business feature translation?"

---

### Step 3: Business Feature Translation

**Say:**

"Diagrams are great for architects. But the business side needs a different view — what does this system *do* in their language?"

Use Antigravity to:
1. **Feature Map Table**: "Based on the repository analysis, create a table with three columns: [Technical Component/Module] → [Business Feature Name] → [Current Limitation]. For example: `openai.ChatCompletion.create` → 'AI Code Generation' → 'No rate limiting, shared API key'."
2. **Glossary**: "Create a glossary of technical terms from the OpenClaw codebase for non-technical stakeholders. Include terms they'll hear in meetings: API, token, prompt, embedding, rate limit, etc."

**STOP:** After creating the feature map and glossary, ask: "I've translated the technical components into business language. Review the table and glossary — would this make sense to the CTO or a steering committee? Let me know when you're ready for the final diagram."

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
**STOP:** After creating the artifact, ask: "The feature map is ready with all diagrams. Open `artifacts/as_is_feature_map.md` and check if the Mermaid diagrams render correctly. Any adjustments needed?"

**STOP:** Once confirmed, ask: "All the architecture documentation is complete. Ready to move to Lesson 3.3 where we'll do the gap analysis — comparing what exists vs what's planned vs what stakeholders actually need?"
