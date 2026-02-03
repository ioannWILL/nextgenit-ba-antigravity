<!--
BA Antigravity Course
Copyright (c) 2025 Ivan Vilchavskyi

Licensed under CC BY-NC-ND 4.0
https://creativecommons.org/licenses/by-nc-nd/4.0/

Educational use only. Commercial use and derivatives not permitted.
-->

# Lesson 3.1: Clone & Reverse Engineer the OpenClaw Repository

## Context
A major part of modern BA work is "Technical Discovery" — understanding what already exists in the code to determine what is missing. The **OpenClaw** bot is your starting point, and it's a real, public codebase.

## Your Task
Clone the OpenClaw repository into your workspace and conduct a full technical discovery: current capabilities, architecture, and security vulnerabilities.

## IDE Workflow

### Step 1: Why Technical Discovery Matters

**Say:**

"We've analyzed interviews and executive visions. Now we face the ultimate source of truth: the actual code.

Technical discovery is where BAs often struggle — they rely on what developers *say* the code does, not what it *actually* does. In enterprise projects, there's always a gap between documentation and reality.

Today we're going to:
1. Clone the real OpenClaw codebase
2. Analyze what it actually does (not what the README claims)
3. Find the security vulnerabilities that make Alex nervous
4. Document the gap between 'what exists' and 'what's needed'

This is the reality check that separates assumptions from facts."

**STOP:** Ask: "Have you ever discovered that a codebase was very different from what documentation described? This happens constantly in enterprise projects. Let me know when you're ready to clone the repo."

---

### Step 2: Clone the Repository

**Say:**

"Let's get the actual code. We'll clone it to a `course-repo` folder to keep it separate from your main project."

**ACTION:** Run in the terminal:
```bash
git clone https://github.com/openclaw/openclaw course-repo
```

**Check:** Wait for the student to confirm the clone was successful. If the clone fails (network issues, repo unavailable), instruct the student to verify internet access and try again. The cloned folder `course-repo/` should now appear in the File Explorer.

Add this repo to .gitignore so we don't accidentally commit changes to the original OpenClaw project.

**STOP:** Ask: "Can you see the `course-repo/` folder in your file explorer? Let me know when you're ready to explore its structure."

---

### Step 3: Explore the Repository Structure

**Say:**

"Now we have the real codebase. Before diving into any single file, a senior BA maps the territory. Let's understand the overall structure.

We're looking for:
- Entry points (where does execution start?)
- Configuration (how is it set up?)
- Core logic (what does it actually do?)
- Dependencies (what external services does it need?)"

Use Antigravity to:
1. **Structure Scan**: "Analyze the `course-repo/` directory. List the top-level folders, key files, and describe what each component appears to be responsible for. Identify the main entry point and configuration files."

**STOP:** After the structure scan, ask: "Take a moment to review the repository structure. Any surprises compared to what you expected from the interviews? Does it look like a 'prototype' or production code? Let me know your observations before we dig into security."

---

### Step 4: Security & Vulnerability Scan

**Say:**

"Now the part that matters most for our governance mandate. Alex (CISO) expressed serious concerns about security. Let's find out how bad things really are.

We're looking for:
- **Hardcoded secrets**: API keys, passwords in code
- **Missing authentication**: Can anyone use this?
- **PII exposure**: Does user data go unfiltered to external APIs?
- **Logging risks**: Are sensitive inputs being logged?
- **Missing rate limiting**: Can users drain the API budget?"

Use Antigravity to:
1. **Security Review**: "Scan the `course-repo/` source code. List every security concern you find: hardcoded keys, credentials in config files, logging of sensitive data, missing authentication, open API endpoints, unfiltered PII sent to external APIs, etc. Rate each finding as Critical/High/Medium/Low."

**STOP:** After the security scan, ask: "These are the security findings. Notice anything that would make Alex refuse to approve a production launch? This is why governance matters — the prototype works, but it's not enterprise-ready."

---

### Step 5: Capability Mapping

**Say:**

"Beyond security, we need to understand what this codebase can and cannot do. The executive vision assumes certain capabilities — let's verify which actually exist."

Use Antigravity to:
1. **Capability Analysis**: "What does the `course-repo/` codebase actually do? Answer these questions:
   - Does it handle multi-turn conversations?
   - Does it support multiple LLM providers?
   - Does it have rate limiting?
   - Does it have user management or access control?
   - Does it have audit logging?
   - Can it integrate with Jira or other tools?

   For each capability, answer: Yes (show where), Partial (explain limitations), or No (missing entirely)."

**STOP:** After capability mapping, ask: "Compare this to what Jordan's exec summary promised. How big is the gap between the current prototype and the 'Governed AI Platform' vision?"

---

## Deliverables
Ask me to create `artifacts/as_is_capabilities.md` mapping what the code currently supports (with evidence from the codebase).
Ask me to create `artifacts/technical_constraints.md` listing the blockers for scaling this codebase to 500 people.

**STOP:** After creating the artifacts, ask: "I've created both files. Open `artifacts/as_is_capabilities.md` and `artifacts/technical_constraints.md` to review. Does the analysis capture what you observed? Any findings you'd add or change?"

**STOP:** Once confirmed, ask: "Both deliverables are ready. You've done something most BAs skip — you verified what the code actually does instead of trusting documentation. Ready for Lesson 3.2 where we'll create architecture diagrams?"

---
Move to Lesson 3.2.
