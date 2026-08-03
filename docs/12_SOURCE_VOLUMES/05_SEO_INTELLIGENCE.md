# SEO Intelligence

Documents merged: **54**

This volume consolidates keyword, SERP, entity, intent, topic-cluster, opportunity, competitor, authority, freshness, CTR, metadata, schema, search-demand, and internal-linking drafts.

## Core pipeline

Seed topics → keyword discovery → normalization and metric enrichment → SERP snapshots → intent and entity analysis → clustering → competitor/content-gap analysis → opportunity scoring → content architecture → publication feedback → refresh decisions.

## Key rules

- Preserve provider, locale, device, and collection timestamp for every metric and SERP snapshot.
- Distinguish observed values from estimates.
- Return evidence and confidence with every score.
- Detect cannibalization before creating a new page.
- Prefer create/update/merge/retire decisions over unconditional generation.
- Keep scoring weights project-configurable and versioned.

## Opportunity model

Opportunity scoring combines demand, ranking feasibility, business value, strategic fit, content gap, freshness, and estimated execution cost. A critical confidence or evidence failure prevents automatic production even when the numeric score is high.

## Linking and authority

The link graph combines semantic relevance, topic hierarchy, existing authority, anchor diversity, publication status, and user journey. Recommendations must exclude redirects, unavailable pages, and repetitive anchors.

## Continuous optimization

Ranking, impression, CTR, traffic, conversion, and competitor-change signals generate explainable refresh, consolidation, metadata-test, and internal-link tasks.
