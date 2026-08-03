# AI SEO Operating System

Personal AI-native SEO operating environment for research, opportunity discovery, content production, quality assurance, publishing, and continuous optimization.

## Start here

1. [`docs/00_START_HERE/PROJECT_MANIFEST.md`](docs/00_START_HERE/PROJECT_MANIFEST.md)
2. [`docs/00_START_HERE/ROADMAP.md`](docs/00_START_HERE/ROADMAP.md)
3. The canonical domain Bible relevant to your task
4. [`docs/11_MACHINE/`](docs/11_MACHINE/) for compact Codex-readable context

## Documentation layers

- `docs/00_START_HERE` through `docs/11_MACHINE`: canonical source of truth.
- `docs/12_SOURCE_VOLUMES`: consolidated historical materials from the earlier specification packs.

The historical volumes are intentionally excluded from default AI context loading. Use them only for targeted provenance or to recover decisions that have not yet been migrated into a canonical document.

## Product scope

This repository targets a single trusted operator first. SaaS billing, agency white-label features, complex organization isolation, and enterprise SSO are not part of the initial implementation unless later requirements justify them.

## Core principles

1. Build for one operator first.
2. Prefer a modular monolith before distributed microservices.
3. No page enters production without QA or an explicit override.
4. Every AI execution records model, prompt version, cost, latency, and outcome.
5. Documentation evolves together with the codebase.

## Current phase

Architecture and documentation foundation. The next phase is the first executable vertical slice: project configuration → AI runtime → SEO opportunity → content workflow → QA → publication.
