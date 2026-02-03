# Lesson 1.2: Executive vs Reality Alignment

## Context
The CTO just sent out an "Executive Summary" (see `discovery-results/exec_summary.md`). However, your interview synthesis from Lesson 1.1 might paint a different picture. Senior BAs must bridge the gap between high-level vision and "on-the-ground" technical reality.

## Your Task
Compare the ambitious goals in the `exec_summary.md` with the reality you discovered in the interviews and Slack fragments.

## IDE Workflow

### Step 1: The Executive-Reality Gap

**Say:**

"Here's a truth about enterprise projects: executives have vision, teams have reality. Neither is wrong — but they often don't match.

Jordan's exec summary describes an ambitious 'Governed AI Platform' with a Jan 15 deadline. But the interviews revealed:
- Security concerns that could block the whole project
- Technical debt in the current prototype
- Resource constraints Sam mentioned

Your job isn't to say 'the executive is wrong.' It's to identify the gaps and propose how to close them — or flag what needs to change."

**STOP:** Ask: "Have you experienced the executive-reality gap before? It's one of the most common sources of project failure. Let me know when you're ready to analyze the gaps."

---

### Step 2: Timeline Reality Check

**Say:**

"Let's start with the timeline. Jordan wants an MVP by Jan 15. But is that realistic given what we know?"

Use Antigravity to:
1. **Timeline Analysis**: "Compare the timeline in `discovery-results/exec_summary.md` with the current state of the Jira backlog in `discovery-results/jira_existing.md`. List:
   - What's promised by Jan 15
   - What's currently in progress
   - What hasn't even been started
   - The gap between promise and reality"

**STOP:** After the timeline analysis, ask: "This is the timeline gap. Notice how some features aren't even in the backlog yet? This is where senior BAs add value — surfacing these gaps early, not on Jan 14."

---

### Step 3: Vision vs Security Conflict

**Say:**

"Now the harder question: can the executive vision coexist with security requirements?

Jordan wants 'self-service AI for 500 developers.' Alex wants 'no PII leaving the building.' These might conflict. Let's find out."

Use Antigravity to:
1. **Conflict Analysis**: "What 'directives' from the CTO in `discovery-results/exec_summary.md` are currently impossible given Alex's security requirements in `artifacts/stakeholder_needs.md`? For each conflict:
   - The executive directive
   - The security concern
   - Why they conflict
   - A possible resolution"

**STOP:** After conflict analysis, ask: "These conflicts are real. You can't just ignore security to hit a deadline — that's how breaches happen. But you also can't block the whole project for theoretical risks. Finding the balance is senior BA work."

---

### Step 4: Crafting Executive Questions

**Say:**

"A senior BA doesn't just identify problems — they propose solutions. But sometimes you need more information before you can solve.

We're going to draft questions for Jordan. These aren't 'gotcha' questions. They're clarification questions that help the executive make informed trade-offs."

Use Antigravity to:
1. **Question Drafting**: "Based on the gaps we identified, draft 5 questions for the CTO that would help clarify scope and priorities. Each question should:
   - Reference a specific gap or conflict
   - Offer options (not just 'what do you want?')
   - Help the executive make a decision

   Example: 'The security team requires PII scrubbing before any prompt reaches the LLM. This adds ~200ms latency. Do we prioritize security compliance (accept latency) or request a security exception for the MVP?'"

**STOP:** After drafting questions, ask: "Notice how each question offers options? This is consultative BA work — you're not dumping problems on executives, you're helping them decide."

---

### Step 5: The GIGO Principle

**Say:**

"Before we create the artifacts, a critical principle: **Garbage In, Garbage Out**.

I can synthesize information, draft documents, and find patterns. But I can't verify if something is actually true in your organization.

The artifacts I create are drafts for YOUR review. You must:
- Verify facts I might have misinterpreted
- Add context I don't have
- Correct assumptions that are wrong

AI assistants boost productivity, but they don't replace professional judgment. Every artifact needs your review before it becomes a 'source of truth.'"

**Pro Tip — Viewing Markdown:**

"To view `.md` files in a more readable format, right-click on the file tab and select 'Open Preview'. This renders headings, tables, and formatting properly."

---

## Deliverables
Ask me to create `artifacts/exec_vs_delivery_gap.md` identifying the top 3 misalignments between executive vision and current reality.
Ask me to create `artifacts/questions_for_exec.md` containing 5 sharp questions you would ask the CTO to clarify scope and priorities.

**STOP:** After creating the artifacts, ask: "Review both artifacts:
- `artifacts/exec_vs_delivery_gap.md`: Are these the gaps you'd flag to a steering committee?
- `artifacts/questions_for_exec.md`: Would these questions help Jordan make decisions?

Remember: GIGO. These are drafts for your review."

**STOP:** Once confirmed, ask: "Executive alignment analysis complete. You've identified where vision meets reality. Ready for Lesson 1.3 where we'll connect to real Jira (optional) or Lesson 1.4 to create the discovery backlog?"

---
Move to Lesson 1.3.
