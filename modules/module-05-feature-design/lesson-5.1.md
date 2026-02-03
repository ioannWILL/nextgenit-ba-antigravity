<!--
BA Antigravity Course
Copyright (c) 2025 Ivan Vilchavskyi

Licensed under CC BY-NC-ND 4.0
https://creativecommons.org/licenses/by-nc-nd/4.0/

Educational use only. Commercial use and derivatives not permitted.
-->

# Lesson 5.1: Feature Decomposition

## Context
"Governed AI" is too big. We need to break it down into smaller, shippable components for the engineering team. This is "Epics to Stories" work.

## Your Task
Decompose the "Governed AI" product into 3 major sub-features (e.g., Auth & Identity, PII Filter Service, Usage Dashboard).

## IDE Workflow

### Step 1: Why Decomposition Matters

**Say:**

"We've written requirements, business rules, and a risk register. But if you hand an engineer a 50-page requirements document and say 'build this,' they'll freeze. The BA's job is to break big features into small, shippable pieces.

This is where we translate business requirements into engineering work:
- **Epics**: Large features that deliver business value (e.g., 'User Authentication')
- **Stories**: Smaller pieces that can be built in a sprint (e.g., 'SSO Login Flow')
- **Tasks**: Technical sub-work within a story (e.g., 'Configure SAML provider')

The hierarchy matters because it maps to how Agile teams plan and track work."

**STOP:** Ask: "Have you worked with Epic/Story/Task hierarchies before? Understanding this structure is essential for communicating with engineering teams. Let me know when you're ready to decompose the features."

---

### Step 2: Identifying Major Sub-Features

**Say:**

"Let's look at what we're building. From the requirements and gap analysis, the 'Governed AI' platform has several major components:

1. **Auth & Identity**: SSO integration, RBAC enforcement, session management
2. **PII Filter Service**: Input scanning, pattern detection, override workflow
3. **Audit Logging**: Event capture, storage, query interface
4. **Usage & Quotas**: Token tracking, quota enforcement, dashboards
5. **Jira Integration**: Ticket creation, artifact linking

Each of these is an Epic. Now we need to break one down to show the pattern."

Use Antigravity to:
1. **Decomposition**: "Take the 'Audit Logging' requirement from `artifacts/functional_requirements.md` and decompose it into an Epic with 4-5 User Stories. For each story, list 2-3 technical tasks. Format as a hierarchy:
   - Epic: [Name]
     - Story 1: [Name]
       - Task 1.1: [Technical work]
       - Task 1.2: [Technical work]
     - Story 2: [Name]
       - ..."

**STOP:** After the decomposition, ask: "This is the Audit Logging epic broken down. Notice how each story is small enough to build in a sprint, but each task is specific enough for an engineer to estimate? Does this level of granularity make sense?"

---

### Step 3: Full Feature Breakdown

**Say:**

"Now let's apply the same pattern to all major features. This becomes your feature breakdown document — the roadmap engineering will use to plan sprints."

Use Antigravity to:
1. **Full Breakdown**: "Create a complete feature breakdown for the Governed AI platform. Include all 5 major epics (Auth & Identity, PII Filter Service, Audit Logging, Usage & Quotas, Jira Integration). For each epic, provide 3-4 stories with tasks. Reference the requirements from `artifacts/functional_requirements.md` to ensure coverage."
2. **Dependency Flags**: "For each epic, note which other epics it depends on. For example, 'Audit Logging' depends on 'Auth & Identity' being complete (need user context to log)."

---

## Deliverables
Ask me to create `artifacts/feature_breakdown.md` with a hierarchy of Epics, Stories, and Tasks.

**STOP:** After creating the artifact, ask: "The feature breakdown is ready. Open `artifacts/feature_breakdown.md` and review:
- Is each story small enough to complete in a 2-week sprint?
- Are the dependencies between epics clear?
- Does this cover all the requirements from Phase 4?

This document becomes the input for sprint planning. Let me know when you're ready for Lesson 5.2 — User Stories with Gherkin acceptance criteria."

---
Move to Lesson 5.2.
