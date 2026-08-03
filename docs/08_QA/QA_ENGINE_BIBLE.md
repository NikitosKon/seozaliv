# QA Engine Bible

## Purpose

Prevent low-value, unsafe, misleading, incomplete, or technically invalid assets from reaching publication.

## Quality dimensions

- Search intent fit
- Content completeness
- Evidence and factual confidence
- Original value
- Readability and structure
- SEO metadata and semantics
- Internal linking
- Conversion readiness
- Technical correctness
- Localization

## Rule types

- Deterministic checks
- Heuristic checks
- AI-assisted evaluations
- External validation checks

## Severity

- Blocker
- Critical
- Major
- Minor
- Advisory

A blocker cannot be hidden by a high aggregate score.

## Autofix

Only low-risk deterministic fixes may apply automatically. Material claims, meaning changes, link destination changes, and publishing actions require review or explicit policy approval.

## Overrides

An override records the operator, reason, affected rule, original result, and expiration or review condition.

## Regression

Rule changes require fixtures covering passing cases, failing cases, edge cases, and false-positive analysis.
