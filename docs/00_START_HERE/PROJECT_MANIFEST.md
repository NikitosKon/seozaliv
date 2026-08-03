# Project Manifest

## Project

**AI SEO Operating System — Personal Edition**

## Purpose

A private operating system for researching SEO opportunities, producing high-value content, validating quality, publishing assets, and continuously improving performance.

## Primary user

One operator. Team, billing, white-label, SSO, and enterprise tenancy are deferred until a proven need appears.

## Core loop

Research → Opportunity scoring → Content plan → Production → QA → Publishing → Analytics → Refresh.

## Recommended implementation shape

- Modular monolith for the control plane
- Independent workers for long-running or externally rate-limited jobs
- Next.js web interface
- Go platform backend
- Python AI and analysis runtime
- PostgreSQL system of record
- Redis cache and task coordination
- Object storage for generated assets and evidence
- Qdrant for semantic retrieval
- ClickHouse introduced only when PostgreSQL analytics becomes insufficient

## Current phase

Architecture normalization and implementation preparation.
