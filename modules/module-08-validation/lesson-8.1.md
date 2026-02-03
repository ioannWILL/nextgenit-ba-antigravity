# Lesson 8.1: UAT & Acceptance

## Context
User Acceptance Testing (UAT) is the final gate. Does the software do what the BA said it should do?

## Your Task
Create a UAT Plan and an Acceptance Checklist to verify that the engineers built the "PII scrubbing" and "RBAC" correctly.

## IDE Workflow

### Step 1: Why UAT Matters for BAs

**Say:**

"Development is done. Engineers say 'it works.' But does it work *the way stakeholders expected*? That's what UAT answers.

As the BA, you're in a unique position:
- You wrote the requirements
- You know what stakeholders actually meant
- You can catch 'technically correct but wrong' implementations

UAT isn't just testing — it's *validation that the right thing was built*. The BA often writes the UAT plan because they understand the business intent behind each requirement."

**STOP:** Ask: "UAT is where 'it works' meets 'it's what we asked for.' Have you seen features that passed all unit tests but failed UAT because they didn't match expectations? Let me know when you're ready to design the UAT plan."

---

### Step 2: Designing UAT Test Cases

**Say:**

"UAT test cases are different from unit tests:
- Unit tests: 'Does this function return the right value?'
- UAT tests: 'Can a user complete their job using this feature?'

For the Governed AI platform, key UAT scenarios:

1. **PII Filter**: 'As Alex (CISO), I verify that PII is blocked and logged'
2. **RBAC**: 'As a contractor, I verify I cannot access admin settings'
3. **Quotas**: 'As a developer, I verify I see a warning at 80% usage'
4. **Audit**: 'As security, I verify I can trace any prompt to a user'

Each test case maps to a business rule or user story."

Use Antigravity to:
1. **UAT Test Cases**: "Generate 5 UAT test cases based on `artifacts/business_rules.md` and `artifacts/user_stories.md`. For each test case:
   - Test ID
   - Description: What business scenario is being tested
   - Preconditions: What must be true before the test
   - Steps: Numbered actions the tester performs
   - Expected Result: What should happen (specific, observable)
   - Pass/Fail Criteria: How we know it passed

   Prioritize tests for PII filtering, RBAC enforcement, and quota warnings."

**STOP:** After generating the test cases, ask: "These are business-focused tests, not technical tests. Notice how each one relates to something a stakeholder cares about? Alex would run the PII test, Sam would verify quotas work. Does this coverage feel complete?"

---

### Step 3: Acceptance Checklist

**Say:**

"Beyond individual tests, we need an acceptance checklist — the 'sign-off criteria' for the Product Owner.

This checklist answers: 'What must be true before we go live?'

Categories:
- **Functional**: Core features work as specified
- **Security**: Alex's requirements are met
- **Performance**: Response times meet NFRs
- **Documentation**: User guides are ready
- **Training**: Support team is briefed"

Use Antigravity to:
1. **Acceptance Checklist**: "Create an acceptance checklist for the Governed AI MVP. Include:

   **Functional Acceptance**
   - [ ] All Priority 1 user stories pass UAT
   - [ ] PII filter blocks known PII patterns
   - [ ] RBAC enforces role boundaries
   ...

   **Security Acceptance**
   - [ ] Audit logs capture all events
   - [ ] No PII in logs (verified by security)
   ...

   **Operational Readiness**
   - [ ] Runbook documented
   - [ ] Monitoring configured
   - [ ] Support team trained
   ...

   Format as a sign-off document with space for signatures."

**STOP:** After generating the checklist, ask: "This checklist is what Jordan and Alex sign before go-live. It's the formal 'we agree this is ready' document. Would this give the steering committee confidence?"

---

### Step 4: Tracing UAT to Requirements

**Say:**

"One more step: ensure every requirement has at least one UAT test covering it. This is 'requirements traceability' — proving we tested what we said we'd build."

Use Antigravity to:
1. **Coverage Matrix**: "Create a requirements-to-UAT traceability matrix:
   | Requirement ID | Description | UAT Test ID | Status |
   |---------------|-------------|-------------|--------|
   | FR-001 | SSO Authentication | UAT-001 | Pending |
   | FR-003 | PII Detection | UAT-003 | Pending |
   ...

   Flag any requirements without UAT coverage — these are gaps."

**STOP:** After generating the coverage matrix, ask: "Any requirements without test coverage? Those are risks — we can't prove they work. Should we add tests or accept the risk?"

---

## Deliverables
Ask me to create `artifacts/uat_plan.md` with test cases and coverage matrix.
Ask me to create `artifacts/acceptance_checklist.md` with sign-off criteria.

**STOP:** After creating the artifacts, ask: "UAT plan and acceptance checklist are ready. Review:
- `artifacts/uat_plan.md`: Are the test cases comprehensive? Do they cover the risky areas from the risk register?
- `artifacts/acceptance_checklist.md`: Would you feel confident signing this as 'ready for production'?

This is the validation gate — pass this, and the project is ready for launch. Ready for the Executive Readout in Lesson 8.2?"

---
Move to Lesson 8.2.
