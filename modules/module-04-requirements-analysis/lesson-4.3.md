# Lesson 4.3: Edge Cases & Risk Analysis

## Context
High-risk AI projects fail on the edges. What if the user submits a 100MB file? What if the LLM provider goes down? What if it hallucinated hardcoded credentials?

## Your Task
Identify 5 high-impact risks and define mitigation strategies.

## IDE Workflow
Use Antigravity to:
1.  **Red Teaming**: "Act as a malicious developer trying to bypass the PII filter in our system. How would you do it? Suggest the requirement to block this."
2.  **Risk Mitigation**: "For each risk in my `artifacts/risk_register.md`, help me write a technical and a process-based mitigation."

## Deliverables
Ask me to create `artifacts/risk_register.md`.

**STOP:** After creating the artifact, ask: "The risk register is complete. Open `artifacts/risk_register.md` and review the identified risks and mitigations. Any edge cases you think we missed?"

**STOP:** Once confirmed, ask: "Phase 4 is complete. You now have a solid requirements foundation — functional requirements, NFRs, business rules, RBAC matrix, and a risk register. Ready to move to Phase 5 — Feature Design? Type `/ba-5` when you're set."

---
**Phase 4 Complete.**
You have a solid foundation of requirements.
Next: Phase 5 — Feature Design (The "Governed AI" Feature).

When you're ready to start Phase 5, type:
```
/ba-5
```
