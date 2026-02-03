# Lesson 3.1: Clone & Reverse Engineer the OpenClaw Repository

## Context
A major part of modern BA work is "Technical Discovery" — understanding what already exists in the code to determine what is missing. The **Clawd Bot** prototype is your starting point, and it's a real, public codebase.

## Your Task
Clone the OpenClaw repository into your workspace and conduct a full technical discovery: current capabilities, architecture, and security vulnerabilities.

## IDE Workflow

### Step 1: Clone the Repository

**Say:**

"Before we can analyze anything, we need the actual code. Let's clone the OpenClaw repository — this is the real Clawd Bot prototype that developers have been running."

**ACTION:** Run in the terminal:
```bash
git clone https://github.com/openclaw/openclaw course-repo
```

**Check:** Wait for the student to confirm the clone was successful. If the clone fails (network issues, repo unavailable), instruct the student to verify internet access and try again. The cloned folder `course-repo/` should now appear in the File Explorer.

**STOP:** Ask the student: "Can you see the `course-repo/` folder in your file explorer? Let me know when you're ready to explore its structure."

---

### Step 2: Explore the Repository Structure

**Say:**

"Now we have the real codebase. Before diving into any single file, a senior BA maps the territory. Let's understand the overall structure."

Use Antigravity to:
1. **Structure Scan**: "Analyze the `course-repo/` directory. List the top-level folders, key files, and describe what each component appears to be responsible for."

**STOP:** After presenting the structure scan, ask the student: "Take a moment to review the repository structure. Any surprises compared to what you expected from the interviews? When you're ready, we'll dig into the security concerns."

---

### Step 3: Security & Vulnerability Scan

**Say:**

"Now the part that matters most for our governance mandate. Let's find out how bad things really are."

Use Antigravity to:
1. **Security Review**: "Scan the `course-repo/` source code. List every security concern you find: hardcoded keys, credentials in config files, logging of sensitive data, missing authentication, open API endpoints, etc."
2. **Capability Mapping**: "What does this codebase actually *do*? Does it handle multi-turn conversations? Does it support multiple LLM providers? Does it have any rate limiting, user management, or access control? Document the findings."

---

## Deliverables
Ask me to create `artifacts/as_is_capabilities.md` mapping what the code currently supports.
Ask me to create `artifacts/technical_constraints.md` listing the blockers for scaling this codebase to 500 people.

---
**STOP:** After creating each artifact, ask: "I've created the file. Please open it and review the contents. Does the analysis capture what you observed? Let me know if you want any changes or if we should move forward."

**STOP:** Once both artifacts are confirmed, ask: "Both deliverables are ready. Have you had a chance to review them? When you're set, we can proceed to Lesson 3.2 where we'll create architecture diagrams."
