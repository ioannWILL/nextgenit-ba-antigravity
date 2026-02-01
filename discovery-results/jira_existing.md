# Jira Export: Project CLAWD (Legacy)

**Status Report**
Total Tickets: 12
Open: 10
Closed: 2

## Backlog

| Key | Summary | Status | Assignee | Priority |
|-----|---------|--------|----------|----------|
| CLAW-45 | **Refactor bot.py into classes** | 🔴 BLOCKED | Mike | Low |
| CLAW-32 | Add support for GPT-4-Turbo | 🟢 Open | Mike | High |
| CLAW-21 | Fix "Rate Limit Exceeded" crashes | 🟢 Open | Unassigned | Critical |
| CLAW-19 | UI: Create a simple React frontend | 🟡 To Do | Jenny | Medium |
| CLAW-12 | **SECURITY: Stop logging prompts to stdout** | 🔴 Open | Mike | Critical |
| CLAW-08 | Add ability to read local files | ✅ Done | Mike | - |

## Comments

**On CLAW-19 (React Frontend)**:
*Jenny*: "I can't start this until the backend exposes a REST API. Currently it's just a CLI script."
*Mike*: "I don't have time to build an API server using Flask. I'm busy with the main product."

**On CLAW-12 (Security Logging)**:
*Alex (Sec)*: "Why is this still open?? It's been 2 months. We are logging code snippets to plain text logs."
*Mike*: "It helps debugging. I'll turn it off later."
