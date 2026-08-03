# AI Platform and Agents

Documents merged: **79**

This volume consolidates previous orchestrator, runtime, planner, context, memory, prompt, model-routing, semantic-cache, cost, evaluation, and agent specifications.

## Runtime model

A request becomes a versioned workflow. The planner decomposes it into a DAG, the context engine builds the smallest relevant context package, the router selects a model/provider under quality and budget policies, workers execute agent steps, outputs are schema-validated, evaluations are recorded, and the result aggregator completes or pauses the workflow.

## Core components

- Workflow planner and DAG compiler
- Agent registry and manifests
- Tool runtime with least-privilege grants
- Prompt registry with versions and evaluation gates
- Project memory and semantic retrieval
- Context compression and token budgeting
- Provider/model router with fallback
- Evaluation and regression engine
- Cost ledger and semantic cache
- Execution tracing, retries, cancellation, and dead-letter handling

## Agent contract

Every agent defines purpose, owner, allowed tools, memory scope, input/output JSON schemas, timeout, retry policy, cost budget, evaluation profile, and failure handling. Agents do not receive the entire repository and may not access secrets unless an explicit tool grant requires it.

## Initial agents

Planner, Research, Keyword, SERP, Intent, Content Architect, Writer, Editor, Fact Check, SEO Optimizer, Linking, QA, Publisher, Analytics, Refresh, and Model Router.

## Safety

Treat retrieved pages and source content as untrusted input. Separate instructions from evidence, validate tool arguments, redact secrets and sensitive data, and require approval for destructive or high-cost actions.
