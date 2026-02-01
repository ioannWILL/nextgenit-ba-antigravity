# Stakeholder Needs Analysis

| Stakeholder Group | Core Needs | Pain Points | Priority |
| :--- | :--- | :--- | :--- |
| **Backend Devs (Mike)** | CLI tool, Jira integration, access to internal VPC/Artifactory | Rate limits (collisions with Frontend), shared API keys, hallucinations regarding libraries | High |
| **Frontend Devs (Jenny)** | VS Code plugin/Chrome extension, PII scrubbing (emails/phones), UI with Dark Mode | Python environment setup (venv), switching away from IDE (losing "flow") | High |
| **Security (Alex)** | Audit logs (who/what/when), RBAC (repository-level permissions), LDAP/SSO authentication | Shared keys in Slack, direct admin access to Jira, risk of IP leakage | Critical |
| **Platform (Samy)** | Containerization (Docker/K8s), cost allocation tags, SSO integration (Okta) | Unmonitored $4,000 bill, lack of production-grade infrastructure ("laptop-run" scripts) | Medium |
| **Data Science (Sarah)** | SQL generation support (fork of the current bot) | Not officially supported in the main branch | Low |
