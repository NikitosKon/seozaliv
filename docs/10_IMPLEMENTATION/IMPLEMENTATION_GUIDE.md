# Implementation Guide

## Build order

1. Repository and local infrastructure
2. Project configuration and provider credentials
3. Workflow and task runtime
4. AI execution accounting
5. Keyword and SERP ingestion
6. Opportunity scoring
7. Content research, briefs, and versions
8. QA engine
9. Publishing connector
10. Analytics and refresh loop

## First vertical slice

The first usable slice should allow the operator to:

1. Create a project.
2. Add or import a keyword.
3. Run research and SERP analysis.
4. Produce an explainable opportunity score.
5. Generate a brief and draft.
6. Run QA.
7. Review and publish manually.
8. Observe workflow cost and result history.

## Definition of done

Every completed feature includes:

- documented behavior and acceptance criteria
- migration when persistent data changes
- typed API or task contract
- automated tests
- structured logs and metrics
- failure and retry behavior
- security review proportional to risk
- updated project brain

## Development rules

- Inspect before editing.
- Prefer small patches.
- Do not mix unrelated refactors.
- Keep domain logic independent of frameworks.
- Never store prompts, keys, or environment-specific values directly in application code.
