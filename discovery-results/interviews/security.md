# Security & Compliance Interview (Alex - CISO Office)
Date: 2025-10-10
Status: HIGH CONCERN

**Overview**:
Alex is very skeptical about the "Clawd Bot" rollout.

**Requirements**:
1.  **NO ANONYMOUS ACCESS**. Every request must be tied to an LDAP user.
2.  **Audit Log**: We need to see exactly *who* asked *what* and *when*. If code leaks, we need to trace it.
3.  **Data Residency**: Where is the model hosted? US or EU? If IT's public OpenAI, do we have the enterprise "zero retention" policy active?
    *   *Note: I don't think the current prototype has this.*
4.  **RBAC**: Contractors should NOT be able to ask questions about the `billing-core` repository. The bot needs to know permissions.

**Red Flags**:
- "I heard developers are sharing an API key in a pinned Slack message. This must stop immediately."
- "The proposed architecture diagram shows the bot having 'admin' access to Jira. unacceptable. Needs least privilege."

**Blocker**:
- "I will not sign off on the release until I see the PII scrubbing logic."
