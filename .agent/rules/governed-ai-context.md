# Governed AI / Clawd Bot Course Context

## The Storyline (Capstone)
"Your company adopted the **Clawd bot** experimentally. It's a powerful AI coding assistant that developers love, but it was built as a 'messy' prototype. Now, leadership wants to roll it out company-wide inside our **Internal Developer Platform (IDP)**. Your task as a Senior Business Analyst is to adapt it for enterprise use: productizing it with security, governance, and professional integration."

---

## 1. Technical Baseline: Clawd Bot (Real Repository)
We are using the **OpenClaw** (Clawd bot) public repository as our technical foundation.
- **Repository:** `https://github.com/openclaw/openclaw`
- **Purpose:** Real codebase for reverse engineering, architecture analysis, and gap identification. This is NOT a simulated project — the student clones the actual repository.
- **Why it works:** Already functional, AI-centric, and realistic for internal platform adoption.
- **How it's used:** In Module 3, the student clones this repository into the workspace and uses Antigravity to analyze the code, generate architecture diagrams, identify security gaps, and map existing capabilities to business features.

### New Features Context
All new enterprise features discussed during the course (RBAC, Audit Logging, PII Scrubbing, Quotas, SSO) are designed as **additions and enhancements to this actual codebase**. Requirements, user stories, and architecture diagrams should reference the real repository structure — not hypothetical components.

---

## 2. Your Role: Senior Business Analyst
You are the bridge between the "Wild West" experimental script and a governed corporate platform. You report to the **Director of Engineering Platform**.

### Your Core Tasks:
1.  **Reverse Engineer:** Clone and analyze the OpenClaw repository — understand what it actually does (Inputs/Outputs, Architecture, Limitations).
2.  **Identify Gaps:** Find the missing "Enterprise" features (Auth, RBAC, Audit, Governance) by comparing the real codebase to stakeholder needs.
3.  **Design for Scale:** Define new features that allow 500+ engineers to use AI safely, mapped to the existing architecture.
4.  **Drive Delivery:** Use the Atlassian MCP to push requirements into Jira.

---

## 3. Product Vision: The Governed AI Platform
The final product is an **Internal AI Assistant with Governance**, built on top of the existing OpenClaw codebase.

### Key Features to Implement:
- **Role-Based Access Control (RBAC):** Not all users have the same powers (Viewer vs Contributor vs Admin).
- **Audit Log & Compliance:** Tracking who asked what, when, and which files were affected.
- **PII Scrubbing Middleware:** Automated detection and redaction of sensitive data before prompts reach the LLM.
- **Prompt Templates:** Shared company standards for story generation, refactoring, and code explanation.
- **Jira Integration (via MCP):** Generating tickets, code context, and ACs directly from AI responses.
- **Usage Limits & Cost Control:** Per-user and per-team quotas to manage API spend.

---

## 4. Key Artifacts for BAs:
Throughout this course, you will generate (all stored in `artifacts/`):

### Phase 1 — Discovery:
- `stakeholder_needs.md` (Interview Synthesis)
- `assumptions_risks.md` (Risk Identification)
- `exec_vs_delivery_gap.md` (Executive Alignment)
- `questions_for_exec.md` (CTO Clarifications)
- `discovery_backlog.md` (Discovery Spikes)

### Phase 2 — Problem Framing:
- `problem_statement.md` (Problem/Impact/Vision)
- `success_metrics.md` (North Star KPIs)
- `scope_definition.md` (MoSCoW Prioritization)
- `out_of_scope.md` (Explicit Exclusions)

### Phase 3 — Reverse Engineering:
- `as_is_capabilities.md` (Current Feature Map)
- `technical_constraints.md` (Scaling Blockers)
- `as_is_feature_map.md` (Architecture Diagram — Mermaid)
- `gap_analysis.md` (Jira vs Code vs Discovery Delta)

### Phase 4 — Requirements:
- `functional_requirements.md` (10+ FRs)
- `nfr.md` (Non-Functional Requirements)
- `business_rules.md` (Token Quotas, Data Classification)
- `roles_permissions_matrix.md` (RBAC Matrix)
- `risk_register.md` (Edge Cases & Mitigations)

### Phase 5 — Feature Design:
- `feature_breakdown.md` (Epic/Story/Task Hierarchy)
- `user_stories.md` (Stories with Gherkin ACs)
- `login_flow.feature` (Gherkin Feature File)
- `data_model.md` (Audit Log Schema)
- `integration_flows.md` (Jira API Integration)

### Phase 6 — UX Validation:
- `wireframes.md` (Textual Wireframes)
- `preview.html` (HTML/Tailwind Mockup)
- `local_prototype.html` (Interactive Prototype)
- `ux_feedback.md` (Friction Points)

### Phase 7 — Delivery:
- `delivery_plan.md` (Phased Rollout)

### Phase 8 — Validation:
- `uat_plan.md` (Test Cases)
- `acceptance_checklist.md` (PO Sign-off)
- `exec_readout.md` (Executive Summary)

---

## 5. Course Philosophy
- **No "Toy" Cases:** Everything is based on a real, working repository (OpenClaw).
- **Reality Checks:** You must deal with technical debt and "messy" interview notes.
- **IDE-First:** You are doing the work inside an Agentic IDE, using AI as a thinking partner, not just a document generator.
- **Architecture Awareness:** New features are designed to extend the real codebase, not exist in isolation.

---

**Use this context for all modules. Every task should feel like a high-stakes transition from an experimental script to an enterprise-grade platform.**
