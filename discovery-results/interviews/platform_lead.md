# Interview: Samy (Platform Engineering Lead)

**Vision**: "Clawd Bot" should be a microservice in our Internal Developer Platform (IDP).

**Technical Needs**:
- Must be containerized (Docker).
- Must emit metrics (Prometheus) for token usage and latency.
- "We are moving everything to K8s. The current script running on Mike's laptop is not 'production'."

**Integration**:
- We use Backstage.io as our developer portal. Can we embed the bot there?
- "I don't want to manage a separate user database. It must use Okta/SSO."

**Cost**:
- "Last month's OpenAI bill was $4,000 and we don't know who spent it. The finance team is breathing down my neck. We need cost allocation tags."

**Conflict**:
- Samy thinks the bot should essentially be a "smart search" for documentation.
- The devs (Mike/Jenny) think it should be a "code generator".
- *Gap identified*: Search vs Generation expectations.
