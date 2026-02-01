# Company Overview: NextGen IT

**Founded:** 2012
**Headquarters:** Austin, TX
**Industry:** Enterprise Software / FinTech
**Employees:** 1,200 (500 in Engineering & Product)

## The Mission
"To empower developers and financial analysts with secure, governed AI tools that accelerate innovation without compromising compliance."

## Organizational Structure
- **CTO Office:** Responsible for the AI Strategy and the "Clawd Bot" experimental rollout.
- **Engineering Platform Team:** Owns the Internal Developer Platform (IDP) and the Backstage.io integration.
- **CISO Office:** Sets security policy, PII filtering requirements, and LDAP/Okta integration standards.
- **Business Operations:** Tracks API costs, token usage, and per-team quotas.

## Current State: The "Wild West"
Engineering has been using a prototype called **Clawd Bot** for the past 6 months. It has significantly improved velocity, but it currently runs as a standalone Python script with:
- Shared API keys in Slack.
- No visibility into what code is being sent to external models.
- No user-based permissions.
- Unpredictable costs.

## Strategic Goal: The "Governed AI" Initiative
The primary objective for Q1 is to "productize" Clawd Bot. This means moving it from a developer's local script to a hardened, enterprise-grade service available via the IDP. 

---

## Your Stakeholders
- **Mike Rodriguez (CTO):** Wants speed and ROI. "The AI must be available to everyone by Jan 15."
- **Alex Chen (CISO):** Wants control. "I will shut this down if I see one more API key in a clear-text log."
- **Samy (Platform Lead):** Wants stability. "It must be a containerized microservice integrated with Okta."
- **Jenny (Frontend Lead):** Wants usability. "I want a dark mode UI and a VS Code extension, not just a CLI."

---

## Market Position
NextGen IT is a global leader in secure financial software. We cannot afford the risks associated with public AI tools. We must build our "Internal Moat" by hosting and governing our own AI services.
