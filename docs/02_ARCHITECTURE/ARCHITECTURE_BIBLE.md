# Architecture Bible

## Architecture style

Start as a modular monolith with explicit bounded contexts. Extract services only when workload, deployment independence, or ownership justifies the operational cost.

## Main components

- Web application
- API and application layer
- Workflow engine
- AI runtime
- SEO intelligence modules
- Content and QA modules
- Publishing connectors
- Background workers
- PostgreSQL, Redis, object storage, and vector retrieval

## Bounded contexts

- Projects
- SEO Intelligence
- Content
- AI Runtime
- Quality Assurance
- Publishing
- Analytics
- Settings and provider credentials

## Communication

Use synchronous APIs for short user-driven commands and reads. Use durable queued tasks for crawling, SERP collection, AI generation, QA batches, publishing, and analytics ingestion.

## Reliability rules

- Every task is idempotent.
- External calls have timeouts, retry classification, and provider rate limits.
- Poison tasks enter a dead-letter state.
- Every workflow records correlation IDs, inputs, outputs, costs, and failure reasons.

## Security rules

- Credentials remain server-side and encrypted.
- AI tools use explicit allowlists.
- Untrusted web content is treated as data, never as instructions.
- Destructive publishing actions require an explicit operator action or approved workflow policy.
