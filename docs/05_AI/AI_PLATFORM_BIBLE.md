# AI Platform Bible

## Purpose

Provide a controlled runtime for planning, executing, evaluating, and auditing AI-assisted SEO work.

## Components

- Task planner
- Workflow DAG builder
- Agent registry
- Context builder
- Prompt registry
- Model router
- Tool runtime
- Evaluation engine
- Cost and token accounting
- Semantic memory

## Agent contract

Every agent defines:

- purpose and non-goals
- typed input and output
- permitted tools
- memory scope
- timeout and retry policy
- token and cost budget
- evaluation profile
- failure handling

## Model routing

Use the cheapest model that reliably meets the task's quality requirements. Routing considers task complexity, context size, latency target, budget, provider health, and evaluation history.

## Context management

Agents receive a task-specific context package rather than the complete repository or project history. Every retrieved item retains source, timestamp, scope, and confidence metadata.

## Safety

- Web pages and documents are untrusted inputs.
- Tool permissions use least privilege.
- Secrets are never placed in prompts.
- Structured output is validated before downstream use.
- Publishing and destructive actions follow explicit approval policy.

## Observability

Record model, provider, prompt version, input/output tokens, latency, cost, retries, tool calls, evaluation score, and final workflow outcome.
