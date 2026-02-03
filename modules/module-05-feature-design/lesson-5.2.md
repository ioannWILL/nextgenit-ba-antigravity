<!--
BA Antigravity Course
Copyright (c) 2025 Ivan Vilchavskyi

Licensed under CC BY-NC-ND 4.0
https://creativecommons.org/licenses/by-nc-nd/4.0/

Educational use only. Commercial use and derivatives not permitted.
-->

# Lesson 5.2: User Stories & ACs (Gherkin)

## Context
Developers need precision. "The system should be secure" is not a requirement. "Given a user is not an admin, when they try to access logs, then they see a 403 error" is.

## Your Task
Write 5 User Stories with detailed Acceptance Criteria (AC) using the Gherkin format (Given/When/Then).

## IDE Workflow

### Step 1: The User Story Format

**Say:**

"User stories are the currency of Agile development. A good user story has three parts:

**As a** [role], **I want** [action], **so that** [business value].

The 'so that' clause is often skipped, but it's the most important part. It tells engineers *why* they're building something, which helps them make better decisions when requirements are ambiguous.

Bad: 'As a user, I want to log in.'
Good: 'As a developer, I want to authenticate via company SSO, so that I don't need another password to manage.'

The difference? The second one tells engineers to integrate with existing SSO, not build a custom auth system."

**STOP:** Ask: "The 'so that' clause connects the story to business value. Can you think of a time when missing context caused engineers to build the wrong thing? Ready to write stories for the PII Filter?"

---

### Step 2: Writing Stories for PII Filtering

**Say:**

"Let's write stories for the PII Filter — one of the most critical features Alex (CISO) requested. We need stories that cover:
- The happy path (filter catches PII)
- The unhappy path (false positive blocks legitimate work)
- The edge cases (user override with approval)

Each story needs acceptance criteria that QA can test."

Use Antigravity to:
1. **Story Writing**: "Write 3 User Stories for the 'PII Filtering' feature based on `artifacts/functional_requirements.md` and `artifacts/business_rules.md`. Include:
   - A story for the basic filter (catches PII in prompts)
   - A story for the false positive override flow
   - A story for the audit trail when PII is detected

   Format each as: 'As a [role], I want [action], so that [value].' Include 3 acceptance criteria per story."

**STOP:** After generating the stories, ask: "These stories cover the main PII filter scenarios. Notice how each one has a clear 'so that' clause connecting to security or usability? Review them — any scenarios we missed?"

---

### Step 3: Gherkin Acceptance Criteria

**Say:**

"Acceptance criteria tell QA exactly what to test. The Gherkin format makes them executable — you can literally run them as automated tests.

The format:
```
Given [precondition]
When [action]
Then [expected result]
```

For example:
```
Given a user is logged in as 'Developer'
When they submit a prompt containing an email address
Then the system displays a PII warning
And the prompt is blocked from submission
```

The key is precision. 'The system is secure' isn't testable. 'The system displays error code 403' is."

Use Antigravity to:
1. **Gherkin Scenarios**: "Write Gherkin scenarios for the login flow. Include:
   - Happy path: Successful SSO login
   - Unhappy path: Invalid credentials
   - Unhappy path: Expired session
   - Edge case: User without platform access tries to log in

   Format as a `.feature` file that could be used with Cucumber or similar BDD tools."

**STOP:** After generating the Gherkin scenarios, ask: "These are executable test scenarios. A QA engineer can read these and know exactly what to verify. Notice the 'Given/When/Then' structure? This is how you bridge BA work and QA work. Any scenarios seem ambiguous?"

---

### Step 4: Comprehensive User Stories Document

**Say:**

"Now let's compile all the user stories into a single document. This becomes the primary artifact engineers and QA reference during development."

Use Antigravity to:
1. **Story Compilation**: "Create a comprehensive user stories document covering all major features from `artifacts/feature_breakdown.md`. For each epic, include 2-3 key stories with Gherkin acceptance criteria. Prioritize stories that address:
   - Security requirements (from Alex)
   - Integration requirements (from Sam)
   - Usability requirements (from Priya)"

---

## Deliverables
Ask me to create `artifacts/user_stories.md`.
Ask me to create `artifacts/login_flow.feature` file with your Gherkin scenarios.

**STOP:** After creating the artifacts, ask: "User stories and Gherkin scenarios are done. Review `artifacts/user_stories.md` and `artifacts/login_flow.feature`:
- Are the acceptance criteria testable? (Could a QA engineer verify pass/fail?)
- Do the stories trace back to stakeholder needs?
- Would an engineer know exactly what to build?

Ready for Lesson 5.3 — Data & Integration Analysis?"

---
Move to Lesson 5.3.
