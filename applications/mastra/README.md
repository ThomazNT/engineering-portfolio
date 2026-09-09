# Thomaz Fernandes — TypeScript Product Engineering for Mastra

**Focus:** developer-facing API contracts, PostgreSQL-backed state and product ownership.

My work includes a fiscal-document API consumed by other applications, together with an operations console. I work on the complete integration experience: validation, authentication, provider behavior, errors that consumers can act on and recovery from uncertain outcomes.

## Recommended review order

1. [Fiscal API](../../projects/fiscal-api/README.md): examine the contract between an application and an asynchronous external service.
2. [Verification scope](../../docs/verification.md): inspect how a regression was reproduced using an isolated database.
3. [Engineering workflow](../../docs/engineering-workflow.md): review how I use coding agents and verify generated changes.

## Relevant engineering discussion

An API consumer needs to distinguish invalid input, a confirmed conflict and a request whose result is still unknown. I would walk through how those distinctions influence the returned error, persisted operation state and safe next action.

The same discussion provides a useful starting point for durable operations and developer tooling: what can be retried, what identity survives a retry, what evidence establishes completion and how a user recovers when the external system is unavailable.

My demonstrated stack is TypeScript, React, PostgreSQL and Deno/Supabase. Using coding agents in development is separate from building production AI-agent infrastructure. This portfolio does not claim production Mastra, Kubernetes or large-scale cloud platform experience.

## Application status

Prepared September 9, 2026. The [original Product Engineer posting](https://jobs.ashbyhq.com/Mastra/3b06208b-34fe-4dda-b409-ee3fd9305cc3) returned “Job not found”. Its earlier requirements in the application plan included TypeScript, PostgreSQL, ownership and cloud infrastructure; those details are historical and must be rechecked for a replacement role.

This document is prepared for an equivalent opening and is not a submitted application.

[Back to portfolio](../../README.md)
