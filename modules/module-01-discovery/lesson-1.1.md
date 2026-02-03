<!--
BA Antigravity Course
Copyright (c) 2025 Ivan Vilchavskyi

Licensed under CC BY-NC-ND 4.0
https://creativecommons.org/licenses/by-nc-nd/4.0/

Educational use only. Commercial use and derivatives not permitted.
-->

# Lesson 1.1: Interview Synthesis

## Context
You have just joined the "Governed AI" project. The team has been using a prototype script called "Clawd Bot," but it's a mess of security risks and technical debt. Before we define requirements, we need to understand what our stakeholders actually *need* versus what they *say*.

## Your Task
Analyze the interview notes in `discovery-results/interviews/` and extract the core needs, pain points, and hidden assumptions.

## IDE Workflow

### Step 1: Why Interview Synthesis Matters

**Say:**

"Welcome to the Governed AI project. Before we write a single requirement, we need to understand the people we're building for. This is Discovery — the most underrated phase in BA work.

Here's the reality: stakeholders don't tell you what they need. They tell you what they *think* they need, what their boss told them to ask for, or what they saw a competitor do. A senior BA reads between the lines.

In the `discovery-results/interviews/` folder, you'll find notes from conversations with:
- **Jordan (CTO)**: The executive sponsor with a vision
- **Alex (CISO)**: Security gatekeeper with concerns
- **Sam (Engineering Lead)**: The one who has to build it
- **Priya (Product Manager)**: Represents the end users

Each has different priorities. Some will contradict each other. Your job is to find the truth."

**STOP:** Ask: "Have you reviewed interview notes before and found contradictions between stakeholders? That tension is normal — and valuable. Let me know when you're ready to analyze the interviews."

---

### Step 2: Multi-File Analysis

**Say:**

"Let's use Antigravity's power to analyze multiple files at once. Instead of reading each interview separately, we'll look for patterns across all of them."

Use Antigravity to:
1. **Conflict Detection**: "Analyze all files in `discovery-results/interviews/` and summarize the conflicting needs between Security (Alex) and the Engineering team (Sam). What does Security want that might slow down developers? What do developers want that might create security risks?"

**STOP:** After the conflict analysis, ask: "Conflicts between security and speed are classic. Did you expect these tensions? This is what makes BA work interesting — you have to find solutions that satisfy both sides. Ready to look for common patterns?"

---

### Step 3: Pattern Detection

**Say:**

"Now let's find what everyone agrees on. Common complaints often point to the real problem — not the symptoms people describe."

Use Antigravity to:
1. **Common Themes**: "What is the common technical complaint across all engineering interviews? Is there something everyone mentions, even if they describe it differently?"
2. **Hidden Assumptions**: "What assumptions are stakeholders making that might not be true? For example, does Jordan assume the current prototype can be 'fixed' rather than rebuilt?"

**STOP:** After pattern detection, ask: "Hidden assumptions are gold. They're often the source of project failures — everyone assumed X was true, but nobody verified it. Did any assumptions surprise you?"

---

### Step 4: Structuring the Findings

**Say:**

"Now we organize what we learned into a structured format. This becomes the foundation for all future requirements work.

A good stakeholder needs document has:
- **Who**: The stakeholder group
- **What**: Their core needs (not features — needs)
- **Why**: The pain points driving those needs
- **Priority**: How critical is this to them

The distinction between 'needs' and 'features' is crucial. 'I need a dark mode' is a feature request. 'I work late and bright screens hurt my eyes' is a need. Needs are stable; features are negotiable."

Use Antigravity to:
1. **Needs Synthesis**: "Based on all interviews, create a structured summary of stakeholder needs. For each stakeholder, identify their core need (not a feature), the pain point driving it, and rate the priority (High/Medium/Low)."
2. **Risk Identification**: "What risks did you identify during discovery? These could be technical risks, political risks, or assumption risks."

---

## Deliverables
Ask me to create `artifacts/stakeholder_needs.md` with the following structure:
- **Stakeholder Group**
- **Core Needs**
- **Pain Points**
- **Priority (High/Med/Low)**

Ask me to create `artifacts/assumptions_risks.md` listing at least 3 risks identified during discovery.

**STOP:** After creating the artifacts, ask: "Review `artifacts/stakeholder_needs.md`. Does each need sound like a business problem, not a feature request? Check `artifacts/assumptions_risks.md` — are these the risks you'd flag to a steering committee?"

**STOP:** Once confirmed, ask: "Discovery synthesis complete. You've extracted the real needs from messy interviews. Ready for Lesson 1.2 where we'll compare this reality against the executive's vision?"

---
Move to Lesson 1.2.
