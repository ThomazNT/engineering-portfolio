# Thomaz Fernandes — Backend Product Engineering for TRM Labs

**Focus:** reliable APIs, PostgreSQL integrity and operational support.

My strongest backend work sits at the boundary between a business application and an external provider. I work on API behavior, scoped database operations, duplicate protection, reconciliation and the investigation of production failures.

## Recommended review order

1. [Fiscal API reliability](../../projects/fiscal-api/README.md): transactional numbering, duplicate billing guards and uncertain provider outcomes.
2. [Verification scope](../../docs/verification.md): 20 passing isolated database tests, with explicit limits.
3. [Logistics platform](../../projects/logistics-platform/README.md): canonical state, role boundaries and operational recovery.

## Match to backend product work

| Requirement | Evidence to review |
| --- | --- |
| APIs that serve customer needs | A fiscal integration surface with actionable conflict and recovery behavior. |
| Relational data design | PostgreSQL reservation, scoping and migration tests. |
| Production support | Critical ticket handling and tracing failures across application, database and provider boundaries. |
| Ownership and communication | End-to-end delivery and documentation of technical decisions and recovery limits. |

I would use the number allocation incident to explain how I prioritize a correction: reproduce the failure, locate the broken invariant, remove an unsafe fallback, test the migration and define post-release verification.

My main backend runtime is Deno/Supabase. I do not claim blockchain analytics, analytical database infrastructure or internet-scale throughput from this work. The inspected official posting uses Node.js but states that previous Node.js experience is not mandatory.

## Application considerations

The [official South America posting](https://jobs.ashbyhq.com/trm-labs/ecc944bf-7cb5-48e7-be97-0d3cb45a92e9), reviewed September 9, 2026, remains readable with an application link. It describes a senior role, public APIs and internal support responsibilities. It also specifies six hours of overlap with PST, including 8 a.m.–2 p.m. PST; availability for this schedule must be confirmed before application.

My software role began in January 2026. This portfolio supports a discussion of practical scope and judgment without claiming a longer tenure. No application has been submitted.

[Back to portfolio](../../README.md)
