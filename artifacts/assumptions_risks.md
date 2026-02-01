# Assumptions & Risks

1. **Security & Compliance Blocker**: The CISO (Alex) will block any production release until a robust PII scrubbing logic and comprehensive audit logging are implemented.
2. **Technical Debt / Scalability Gap**: The current "Clawd Bot" is a "spaghetti-code" Python script running on local machines. Migrating this to a production-grade microservice architecture (K8s/Docker) while maintaining current functionality is a significant technical risk.
3. **Intellectual Property (IP) Leakage**: Developers are currently using shared API keys and have already demonstrated unsafe behavior (pasting production JWTs into public AI). There is a high risk of sensitive company code or credentials being leaked to public LLM providers.
4. **Stakeholder Vision Divergence**: There is a clear misalignment between Platform Engineering (who see a "smart search" tool) and Dev Teams (who want a "code generator"). This could lead to a product that satisfies neither group.
5. **Cost Escalation**: Without the technical implementation of cost allocation tags and per-user quotas, OpenAI expenditures will continue to be unmonitored and potentially exceed budgets ($4,000+ monthly).
