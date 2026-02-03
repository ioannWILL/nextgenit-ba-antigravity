# Lesson 4.2: Business Rules & Governance

## Context
AI is expensive and dangerous without rules. How do we ensure "Contractors" don't see "Core" code? How do we stop the "AI bill" from exploding?

## Your Task
Define the Business Rules and the Roles & Permissions Matrix.

## IDE Workflow

### Step 1: Why Business Rules Matter

**Say:**

"Requirements tell engineers what to build. Business rules tell them how the system should *behave* in specific scenarios. These are the policies that govern the platform.

Think about it:
- What happens when a developer hits their daily token limit? Block them? Warn them? Charge their cost center?
- Can a contractor see code from the 'Core Platform' repository? What about during a security incident?
- If the PII filter flags a false positive, can users override it? Who approves?

These aren't features — they're *decisions* that need to be documented. Otherwise, every engineer makes their own interpretation."

**STOP:** Ask: "Business rules are often the hardest part of BA work because they require decisions from stakeholders. Have you encountered situations where unclear business rules caused implementation problems? Let me know when you're ready to draft the rules."

---

### Step 2: Token Usage & Quota Rules

**Say:**

"Let's start with the money problem. Sam mentioned the 'API bill nightmare' — developers burning through tokens with no visibility. We need rules that balance developer productivity with cost control.

Consider:
- Daily vs monthly quotas
- What happens at 80% usage? At 100%?
- Can managers grant exceptions?
- How are overages handled — block, throttle, or alert?"

Use Antigravity to:
1. **Rule Definition**: "Write 5 business rules for 'Token Usage Quotas' in the Governed AI platform. Cover: quota allocation by role, warning thresholds, behavior at limit, exception process, and overage handling. Format each rule as: 'BR-XXX: [Rule name] - When [condition], the system shall [action] because [business rationale].'"

**STOP:** After generating the rules, ask: "These are the quota rules. Notice each one has a business rationale — that's important for when engineers ask 'why?' Review them — are the thresholds reasonable? Too strict might frustrate developers, too loose defeats the purpose."

---

### Step 3: Role-Based Access Control (RBAC) Matrix

**Say:**

"Alex (CISO) was clear: 'Contractors shouldn't see everything, and we need to know who asked what.' This means implementing RBAC — Role-Based Access Control.

An RBAC matrix maps:
- **Roles**: Developer, Lead, Security, Admin, Contractor
- **Permissions**: What each role can do (ask questions, view logs, delete history, change config)

This matrix becomes the source of truth for the engineering team building the auth layer."

Use Antigravity to:
1. **RBAC Matrix**: "Create a markdown table showing the RBAC matrix for the Governed AI platform. Rows: Roles (Developer, Lead, Security Analyst, Admin, Contractor). Columns: Permissions (Submit Prompts, View Own History, View Team History, View Audit Logs, Delete Own History, Override PII Filter, Manage Quotas, System Config). Use ✓ for allowed, ✗ for denied, and 'Approval Required' where applicable. Add a brief justification column."

**STOP:** After generating the matrix, ask: "Here's the RBAC matrix. This is what Alex asked for — clear boundaries on who can do what. Pay attention to the Contractor row — they have limited access by design. Does this match the security requirements from the interviews?"

---

## Deliverables
Ask me to create `artifacts/business_rules.md`.
Ask me to create `artifacts/roles_permissions_matrix.md`.

**STOP:** After creating the artifacts, ask: "The business rules and RBAC matrix are ready. Check `artifacts/business_rules.md` and `artifacts/roles_permissions_matrix.md`.

Key things to verify:
- Do the quota rules align with what Sam described?
- Does the RBAC matrix satisfy Alex's security concerns?
- Are there any edge cases we haven't covered?

Ready for the risk analysis in Lesson 4.3?"

---
Move to Lesson 4.3.
