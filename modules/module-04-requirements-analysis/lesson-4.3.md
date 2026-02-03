# Lesson 4.3: Edge Cases & Risk Analysis

## Context
High-risk AI projects fail on the edges. What if the user submits a 100MB file? What if the LLM provider goes down? What if it hallucinated hardcoded credentials?

## Your Task
Identify 5 high-impact risks and define mitigation strategies.

## IDE Workflow

### Step 1: Why Risk Analysis Matters

**Say:**

"We've written requirements and business rules. But here's the uncomfortable truth: AI systems fail in unexpected ways. A senior BA anticipates these failures *before* they hit production.

Risk analysis isn't about being pessimistic — it's about being prepared. For an AI platform, risks fall into categories:
- **Security risks**: PII leakage, prompt injection, credential exposure
- **Operational risks**: API provider outages, quota exhaustion, data loss
- **Compliance risks**: GDPR violations, audit failures, unauthorized access
- **Technical risks**: Hallucinations, model degradation, integration failures

We'll document these in a risk register — a standard BA artifact that tracks risks, their likelihood, impact, and mitigations."

**STOP:** Ask: "Risk registers are living documents — they get updated throughout the project. Have you worked with risk registers before? Any specific risks you're already worried about based on what we've seen in the codebase?"

---

### Step 2: Red Team Thinking

**Say:**

"Let's think like an attacker. The best way to find vulnerabilities is to try to exploit them. This is called 'red teaming.'

For the PII filter we're planning:
- How would a malicious developer bypass it?
- What if they encode the PII in base64?
- What if they split sensitive data across multiple prompts?
- What if they use homoglyphs (characters that look similar)?

Each attack vector becomes a requirement to block it."

Use Antigravity to:
1. **Red Teaming**: "Act as a malicious developer trying to bypass the PII filter in the Governed AI platform. List 5 attack vectors — how would you sneak sensitive data past the filter? For each attack, suggest a specific requirement that would block it. Format: 'Attack: [description] → Mitigation Requirement: [FR/NFR that blocks it]'."

**STOP:** After the red team analysis, ask: "These are real attack vectors that security teams think about. Notice how each one leads to a concrete requirement? This is how security requirements get written — by thinking like an attacker. Any of these surprise you?"

---

### Step 3: Risk Register Development

**Say:**

"Now let's build the formal risk register. For each risk, we document:
- **Risk ID**: Unique identifier
- **Description**: What could go wrong
- **Likelihood**: Low / Medium / High
- **Impact**: Low / Medium / High / Critical
- **Risk Score**: Likelihood × Impact
- **Technical Mitigation**: Engineering solution
- **Process Mitigation**: Policy or procedure solution
- **Owner**: Who's responsible for monitoring

The combination of technical AND process mitigations is key. Technology alone doesn't solve everything."

Use Antigravity to:
1. **Risk Register**: "Create a risk register for the Governed AI platform with 5 high-impact risks. Include risks from: PII exposure, API provider failure, quota abuse, unauthorized access, and AI hallucination of credentials. For each risk, provide: Risk ID, Description, Likelihood (L/M/H), Impact (L/M/H/Critical), Technical Mitigation, Process Mitigation, and Risk Owner. Format as a markdown table."

**STOP:** After generating the risk register, ask: "Here's the risk register. Notice each risk has both technical AND process mitigations. For example, PII exposure isn't just solved by a filter — it also needs training and incident response procedures. Review the risks — any that should be higher priority?"

---

### Step 4: Connecting Risks to Requirements

**Say:**

"A risk register isn't useful if it sits in a drawer. Each risk should trace to requirements that mitigate it. Let's verify our requirements coverage."

Use Antigravity to:
1. **Traceability Check**: "Review the risks in the risk register against `artifacts/functional_requirements.md` and `artifacts/nfr.md`. For each risk, identify which requirement(s) address it. Flag any risks that don't have corresponding requirements — these are gaps we need to fill."

---

## Deliverables
Ask me to create `artifacts/risk_register.md`.

**STOP:** After creating the artifact, ask: "The risk register is complete. Open `artifacts/risk_register.md` and review:
- Are the risk scores accurate? (Likelihood × Impact)
- Do the mitigations seem feasible?
- Any edge cases or failure scenarios we missed?

This document will be reviewed by Alex (CISO) and the steering committee."

**STOP:** Once confirmed, ask: "Phase 4 is complete. You now have a solid requirements foundation:
- **Functional Requirements**: What the system does
- **Non-Functional Requirements**: How well it performs
- **Business Rules**: How it behaves in specific scenarios
- **RBAC Matrix**: Who can do what
- **Risk Register**: What could go wrong and how we prevent it

These five artifacts form the requirements baseline for engineering. Ready to move to Phase 5 — Feature Design? Type `/ba-5` when you're set."

---
**Phase 4 Complete.**
You have a solid foundation of requirements.
Next: Phase 5 — Feature Design (The "Governed AI" Feature).

When you're ready to start Phase 5, type:
```
/ba-5
```
