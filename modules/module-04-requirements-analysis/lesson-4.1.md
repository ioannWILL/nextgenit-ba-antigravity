# Lesson 4.1: Stakeholder-Driven Requirements

## Context
It's time to write the requirements for the "Enterprise AI Platform" (the replacement for Clawd Bot). You must distinguish between Functional (what it does) and Non-Functional (how it behaves).

## Your Task
Generate a comprehensive set of Functional and Non-Functional Requirements (NFRs).

## IDE Workflow

### Step 1: Understanding Requirements Types

**Say:**

"Before we start writing, let's be clear on what we're producing. In BA work, there are two categories of requirements that engineers need:

- **Functional Requirements (FRs)**: What the system *does*. 'The system shall authenticate users via SSO.' These are testable features.
- **Non-Functional Requirements (NFRs)**: How the system *behaves*. 'The system shall respond to prompts within 2 seconds under normal load.' These are quality attributes.

The gap analysis from Phase 3 told us *what's missing*. Now we translate that into formal requirements that engineers can build against."

**STOP:** Ask: "Does the distinction between functional and non-functional requirements make sense? Any questions before we start drafting?"

---

### Step 2: Functional Requirements from Stakeholder Needs

**Say:**

"Let's pull from the stakeholder interviews. Remember what each person needed:
- **Jordan (CTO)**: Governed AI, usage visibility, enterprise-ready
- **Alex (CISO)**: PII protection, audit trails, access control
- **Sam (Engineering Lead)**: Jira integration, per-user quotas
- **Priya (Product Manager)**: Self-service onboarding, usage dashboards

Each of these translates into functional requirements. We'll focus on Security, User Auth, and Integration — the governance mandate."

Use Antigravity to:
1. **Requirement Generation**: "Based on the stakeholder needs in `artifacts/stakeholder_needs.md` and the gap analysis in `artifacts/gap_analysis.md`, write 10 functional requirements for the 'Governed AI' platform. Each requirement should follow the format: 'FR-XXX: The system shall [action] so that [business value].' Focus on Security, User Authentication, and Jira Integration."

**STOP:** After generating the requirements, ask: "Here are the functional requirements derived from stakeholder interviews. Notice how each one traces back to a specific stakeholder need? Review them — any gaps or requirements that seem out of scope?"

---

### Step 3: Non-Functional Requirements (Quality Attributes)

**Say:**

"Functional requirements tell engineers *what* to build. NFRs tell them *how well* it needs to perform. These are often where projects fail — everyone agrees on features, but nobody defined 'fast enough' or 'secure enough.'

For an AI platform, critical NFRs include:
- **Latency**: How fast must the bot respond? 2 seconds? 10 seconds?
- **Availability**: What's the uptime SLA? 99.9%?
- **Data Residency**: Where can data be stored? EU requirements?
- **Scalability**: 500 users now, but what about 5,000?"

Use Antigravity to:
1. **NFR Drafting**: "Draft non-functional requirements for the Governed AI platform covering: Latency (response time targets), Availability (uptime SLA), Data Residency (where prompts and responses can be stored), and Scalability (concurrent user targets). Use measurable criteria — no vague terms like 'fast' or 'secure'. Format: 'NFR-XXX: [Category] - [Measurable requirement]'."

---

## Deliverables
Ask me to create `artifacts/functional_requirements.md`.
Ask me to create `artifacts/nfr.md`.

**STOP:** After creating the artifacts, ask: "I've drafted both the functional requirements and NFRs. Open `artifacts/functional_requirements.md` and `artifacts/nfr.md` to review. Notice how each requirement is:
- Traceable to a stakeholder need
- Testable with clear acceptance criteria
- Measurable (especially NFRs)

Do these capture the governance mandate from the stakeholder interviews? Let me know when you're ready for Lesson 4.2 — Business Rules & Governance."

---
Move to Lesson 4.2.
