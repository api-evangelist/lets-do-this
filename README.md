# Let's Do This

Let's Do This is an endurance-events marketplace where participants discover and register for mass-participation sport — marathons, road races, trail runs, triathlons, obstacle races and cycling events — across the United Kingdom and the United States. It covers event discovery, entry purchase and management, team entries, memberships, referral credits and discount codes, and works with event organisers and charity partners who list and sell places through it.

Backed by: eqt-ventures — https://www.letsdothis.com/

## API posture (probed 2026-07-19)

Let's Do This publishes **no public API program**. There is no developer portal, API documentation, API reference, OpenAPI/GraphQL schema, SDK, CLI, webhook catalogue, status page or `/.well-known/` discovery document. The marketing site is fully bot-blocked (403); `docs.letsdothis.com` exists but is Vercel SSO-gated (internal). Organiser and charity-partner integrations appear to run through private commercial relationships rather than a self-serve developer surface.

A live GraphQL endpoint at `https://graphql.letsdothis.com/graphql` backs the consumer marketplace — it answers unauthenticated `{__typename}` but has introspection disabled (403), so no schema could be captured. See `graphql/lets-do-this-graphql-endpoint.yml`.

## Artifacts

- `security/lets-do-this-domain-security.yml` — probed TLS/DNSSEC/CAA/SPF/DMARC posture
- `well-known/lets-do-this-well-known.yml` — recorded `/.well-known/` probe results (none published)
- `graphql/lets-do-this-graphql-endpoint.yml` — evidence for the undocumented GraphQL endpoint
- `llms/lets-do-this-llms.txt` — generated llms.txt profile
