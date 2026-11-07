# Beauty Data Lab — Customer Data & Lifecycle Product Concept

An independent, browser-only interactive portfolio prototype by Crystal Thuy Dong. This project demonstrates how I approach marketing technology product requirements across first-party customer data, event taxonomy, audience segmentation, consent enforcement and lifecycle activation.

**This is a synthetic technical concept, not a production CDP, not a customer implementation, and not proof of prior ownership of Braze, Iterable or Salesforce Marketing Cloud.** It does not use real customer data or contact an external service.

## Explore the prototype

[**Open the interactive demo**](https://tdong1919-dev.github.io/beauty-data-lab/) · [View the source](https://github.com/tdong1919-dev/beauty-data-lab)\n\nYou can also open `index.html` locally. No build tools, accounts, credentials or network connections are required.

Try this sequence:

1. In **Customer profiles**, select Maya Chen and turn off email consent.
2. In **Audiences**, select email; Maya will be suppressed from the eligible set.
3. In **Lifecycle journeys**, select Maya and simulate `add_to_cart`; the cart reminder is suppressed because email consent is missing.
4. Re-enable consent, repeat the event and inspect the changed eligibility decision.
5. Explore the **Event taxonomy** contract and **Consent & audit** session log.

The demo models the relationship between signals, customer state, audience rules and governed channel decisions. No actual messages are sent.

## Product management lens

| Product area | Demonstrated interaction | Production considerations not implemented |
| --- | --- | --- |
| Customer profiles | Synthetic IDs, traits, history, channel permissions | Identity graph, merge policies, source lineage |
| Event taxonomy | Named events with required fields and business uses | Collection SDK, schema registry, validation pipeline |
| Segmentation | Tier/interest filters and permission-based exclusion | Real-time computation, audience sync, identity resolution |
| Journeys | Trigger-to-audience-to-consent decision simulation | Channel integrations, throttling, fatigue, messaging orchestration |
| Governance | Session-local log and permission changes | Durable audit, consent sourcing, regional policy enforcement |

### If taking this into a discovery sprint

- Interview Commerce, Data, Integrated Marketing, Privacy and Engineering stakeholders to define the customer identity and activation use cases.
- Produce a data dictionary with properties, sources, purposes, owners, retention, and downstream consumers.
- Prioritize a narrow, consent-safe activation flow with measurable outcomes, quality checks and failure handling.
- Evaluate build versus buy against existing CDP and engagement-platform capabilities before selecting vendors.
- Define acceptance tests for duplicate identities, late and invalid events, consent withdrawal, delivery errors, and rollback.

## Safety and scope

- All profiles and metrics are fictional; email addresses use `.test` domains.
- No backend, API keys, SDKs, tracking pixels or network calls are used.
- All changes reset on refresh or by pressing **Reset example**.
- The implementation intentionally exposes only a conceptual interaction model; it does not contain Marketing OS or Scout source, client records or private JIDOKA architecture.

© 2026 Crystal Thuy Dong. All rights reserved.
