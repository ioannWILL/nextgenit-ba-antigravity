# Lesson 6.2: Interactive Prototype

## Context
Validating flows with stakeholders is easier when they can click things. You'll build a very simple interactive prototype (mocked logic) inside the IDE.

## Your Task
Use Antigravity to build a small web-app prototype that "simulates" a prompt being sent and checked by a PII filter.

## IDE Workflow

### Step 1: Why Prototypes Matter

**Say:**

"A wireframe shows layout. A prototype shows *behavior*. There's a huge difference between:

- Looking at a picture of a PII warning dialog
- Actually typing an email address and seeing the warning appear

Prototypes catch problems that wireframes miss:
- 'Wait, the warning blocks the whole screen? That's annoying.'
- 'I can't dismiss this? What if it's a false positive?'
- 'Where did my prompt go after the warning?'

We're building a *functional prototype* — not production code, but something stakeholders can click through to validate the flow."

**STOP:** Ask: "Prototypes reveal UX issues that requirements documents hide. Have you seen a prototype change stakeholder minds about a feature? Let me know when you're ready to build the PII filter prototype."

---

### Step 2: PII Filter Simulation

**Say:**

"The PII filter is the most critical security feature. Alex needs to see it working. Let's build a prototype that:

1. Shows a chat input
2. Detects if the user types something that looks like PII (email, phone, SSN pattern)
3. Displays a warning *before* the prompt is submitted
4. Gives the user options: Edit prompt, Request Override, or Cancel

This simulates the actual flow without calling any real APIs."

Use Antigravity to:
1. **Prototype Building**: "Build a single-file HTML/JS prototype that simulates the PII filter flow:

   **Requirements:**
   - Text input for prompts
   - Real-time PII detection (check for email patterns like `@`, phone patterns, etc.)
   - When PII detected: Show a warning modal with:
     - What was detected ('Email address found')
     - Options: 'Edit Prompt', 'Request Override', 'Cancel'
   - If 'Request Override' clicked: Show 'Override request sent to Security team' message
   - If no PII: Simulate an AI response after 1 second delay

   Use vanilla JS (no frameworks). Include comments explaining the logic."

**STOP:** After generating the prototype, ask: "This is the PII filter in action. Try it:
1. Type a normal prompt — it should 'send' after a delay
2. Type something with an email address — the warning should appear

Does the warning feel intrusive or helpful? This is the UX question we're validating."

---

### Step 3: Testing the Flow

**Say:**

"Now let's test the prototype against our requirements. Open `artifacts/local_prototype.html` in a browser and try these scenarios:

1. **Happy path**: Type 'How do I write a Python function?' — should work normally
2. **PII detection**: Type 'Send email to john@company.com' — should trigger warning
3. **Override flow**: Click 'Request Override' — should show confirmation

Each of these maps to a user story from Phase 5."

Use Antigravity to:
1. **Test Checklist**: "Create a simple test checklist for the prototype based on the user stories in `artifacts/user_stories.md`. For each PII-related story, list:
   - Test scenario
   - Expected behavior
   - Pass/Fail checkbox

   This becomes the validation script for stakeholder demos."

**STOP:** After creating the checklist, ask: "Run through the test scenarios yourself. Does the prototype behave as expected? Any edge cases where the behavior is unclear or frustrating?"

---

### Step 4: Stakeholder Demo Preparation

**Say:**

"This prototype will be shown to stakeholders — Jordan (CTO), Alex (CISO), Priya (PM). Each cares about different things:

- **Jordan**: Does it look enterprise-ready?
- **Alex**: Does the security warning actually stop PII from being sent?
- **Priya**: Is it usable? Will developers hate it?

Let's prepare talking points for the demo."

Use Antigravity to:
1. **Demo Script**: "Create a short demo script for showing the PII filter prototype to stakeholders. Include:
   - 2-minute walkthrough of the happy path
   - Security demo for Alex (show PII being caught)
   - UX demo for Priya (show the override flow)
   - Questions to ask stakeholders for feedback"

---

## Deliverables
Ask me to create `artifacts/local_prototype.html` with the interactive PII filter simulation.

**STOP:** After creating the artifact, ask: "The interactive prototype is ready. Open `artifacts/local_prototype.html` in a browser and test:
1. Normal prompt — does it simulate a response?
2. Prompt with email — does the warning appear?
3. Override request — does it show confirmation?

This is what you'd demo to Alex to prove the PII filter works. Does the flow feel right? Ready for UX review in Lesson 6.3?"

---
Move to Lesson 6.3.
