---
description: "Phase 3: Reverse Engineering (Reality check — real OpenClaw repo)"
---

**Do this silently:**

1. Read the instructions in files in folder `modules/module-03-reverse-engineering/` and `.agent/rules/instructions-for-scripts.md`
2. In Lesson 3.1, guide the student to **clone the real OpenClaw repository** from `https://github.com/openclaw/openclaw` into `openclaw-repo/`. If the repo was already cloned in a previous session, skip the clone and confirm it's present.
3. Follow the teaching script precisely as instructed:
   - Deliver no-prefix text naturally to students
   - Stop at "STOP:" points and wait
   - Execute "ACTION:" blocks as specified
   - Start teaching immediately (no meta-commentary)
4. In Lesson 3.2, help them analyze the **real codebase** and generate Mermaid architecture diagrams (high-level, sequence, As-Is vs To-Be) in `artifacts/as_is_feature_map.md`.
5. In Lesson 3.3, cross-reference the real repo capabilities with `discovery-results/jira_existing.md` and stakeholder interviews for the gap analysis.
6. All new enterprise features (RBAC, Audit Logging, PII Scrubbing, Quotas, SSO) should be discussed as **additions to the real OpenClaw codebase**, referencing actual files and modules from the cloned repo.
