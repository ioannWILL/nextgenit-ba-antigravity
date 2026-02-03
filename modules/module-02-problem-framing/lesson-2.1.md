<!--
BA Antigravity Course
Copyright (c) 2025 Ivan Vilchavskyi

Licensed under CC BY-NC-ND 4.0
https://creativecommons.org/licenses/by-nc-nd/4.0/

Educational use only. Commercial use and derivatives not permitted.
-->

# Lesson 2.1: Define the Real Problem

## Context
Everyone is asking for "features" (dark mode, VS Code plugin, etc.). But what problem are we *actually* solving for the business? Is it productivity? Is it security? Is it cost control?

## Your Task
Synthesize all Phase 1 artifacts into a formal Problem Statement and define how we will measure success.

## IDE Workflow

### Step 1: Why Problem Statements Matter

**Say:**

"Phase 1 gave us raw material: stakeholder needs, executive gaps, discovery questions. Now we need to distill it into a clear problem statement.

Here's why this matters: without a problem statement, everyone optimizes for different things. Engineers build cool features. Security adds controls. Executives ask for demos. Nobody knows if they're solving the right problem.

A good problem statement has three parts:
1. **The Pain**: What's broken today? (Concrete, not vague)
2. **The Impact**: Why does it matter? (Business cost, not just annoyance)
3. **The Vision**: What does success look like? (Measurable, not aspirational)

Bad: 'We need better AI tools.'
Good: 'Developers spend 3 hours/day on repetitive code tasks, costing $2M/year in productivity. An AI coding assistant could recover 60% of that time while maintaining security compliance.'"

**STOP:** Ask: "Have you written problem statements before? The discipline of defining 'what problem are we solving' prevents scope creep and misaligned expectations. Let me know when you're ready to draft ours."

---

### Step 2: Synthesizing the Pain

**Say:**

"Let's build our problem statement from the evidence we collected. What's actually broken?"

Use Antigravity to:
1. **Pain Synthesis**: "Review `artifacts/stakeholder_needs.md` and `artifacts/exec_vs_delivery_gap.md`. Identify the core pain point that appears across multiple stakeholders. Express it as:
   - The current situation (what's happening)
   - Who is affected (which stakeholders)
   - The cost (time, money, risk, frustration)

   Focus on the problem, not any solution."

**STOP:** After the pain synthesis, ask: "This is the pain we're solving. Does it resonate? If someone asked 'why are we doing this project?' could you point to this pain?"

---

### Step 3: Defining Success Metrics

**Say:**

"A problem statement without metrics is just a complaint. We need to define how we'll know we've succeeded.

For an AI productivity platform, typical metrics include:
- **Adoption**: How many developers use it weekly?
- **Productivity**: How much time saved per developer?
- **Quality**: Does AI-assisted code pass review at the same rate?
- **Security**: Zero PII incidents? Audit compliance?
- **Cost**: ROI compared to API spend?

These become our 'North Star' metrics — the numbers the steering committee will track."

Use Antigravity to:
1. **Metric Design**: "Based on Jordan's vision in the exec summary and the stakeholder needs, propose 3-5 metrics for the Governed AI project. For each metric:
   - Metric name
   - What it measures
   - Current baseline (if known)
   - Target value
   - How to measure it
   - Who owns it

   Balance productivity metrics (what Jordan wants) with security metrics (what Alex wants)."

**STOP:** After defining metrics, ask: "Notice how we have both productivity AND security metrics? That's intentional — we're showing both stakeholder groups that their concerns are being measured. Does this balance feel right?"

---

### Step 4: Crafting the Problem Statement

**Say:**

"Now let's write the formal problem statement. This becomes the anchor for all future scope discussions.

Format:
**The Problem**: [Current pain in one sentence]
**The Impact**: [Business cost or risk]
**The Vision**: [What success looks like]
**Success Metrics**: [How we measure it]

This should fit on one slide or one page. If it takes longer to explain, it's not clear enough."

Use Antigravity to:
1. **Problem Statement Draft**: "Write a formal problem statement for the Governed AI project that:
   - Addresses the CTO's productivity vision
   - Acknowledges Security's governance concerns
   - Is specific enough to reject out-of-scope requests
   - Includes measurable success criteria"

**STOP:** After drafting, ask: "Read the problem statement out loud. Could you explain this to someone who knows nothing about the project? If it's confusing, we need to simplify."

---

### Step 5: Optional Confluence Integration

**Say:**

"Problem statements belong in shared documentation, not just local files. If you have Confluence connected, I can create pages from these artifacts — making them the official 'source of truth' for the project."

---

## Deliverables
Ask me to create `artifacts/problem_statement.md` containing:
- The Problem (The "Pain")
- The Impact (Why it matters now)
- The Vision (The "Future State")

Ask me to create `artifacts/success_metrics.md` listing 3-5 KPIs with baselines and targets.

**STOP:** After creating the artifacts, ask: "Review both artifacts:
- `artifacts/problem_statement.md`: Is the problem clear and specific? Could you use it to reject a feature request that doesn't fit?
- `artifacts/success_metrics.md`: Are the targets realistic? Do we know how to measure them?

Would you like me to create Confluence pages from these artifacts?"

**STOP:** Once confirmed, ask: "Problem framing started. You have a clear problem statement and success metrics. Ready for Lesson 2.2 where we'll define what's in scope and what's not?"

---
Move to Lesson 2.2.
