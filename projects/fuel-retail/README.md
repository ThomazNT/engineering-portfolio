# Fuel Retail — Administrative and Customer Applications

Related React and TypeScript applications support administrative operations and customer workflows for fuel retail. The backend uses PostgreSQL, Supabase and server-side functions for privileged operations and external integrations.

My work spans application delivery, organization context, integrations and production support.

## Two connected product surfaces

The administrative application supports tenant management, operational views, white-label configuration and external service integrations. The customer application maintains an active network context, retrieves the networks available to the user and updates cached data when the user changes network.

This is a product problem as well as a data problem: the interface must make the selected organization clear, while the server enforces access independently.

## Engineering decisions

| Concern | Implementation evidence | Boundary |
| --- | --- | --- |
| Customer network selection | A React context reads available networks and a persisted preference, resolves selection through an RPC and resets queries. | Browser preferences do not grant access. |
| Administrative organization context | A scoped request wrapper adds tenant filtering during selected administrative operations. | This is a UI safeguard, not proof of a complete server authorization boundary. |
| Asynchronous fueling workflows | Callback tests describe staged session transitions and reconciliation endpoints. | Live provider behavior requires a dedicated integration environment. |
| Per-network presentation | White-label provisioning documentation and configuration. | Configuration and secrets must remain separate. |

## A walkthrough I can explain

A customer switches network while viewing operational data. The application resolves the new context, updates the saved selection and resets queries so data is reloaded for that context. I would explain error handling and the server-side checks required to keep this interaction safe.

For an external operation with a missing callback, I would walk through the request identity, stored state and reconciliation path before deciding whether another attempt is appropriate.

## Evidence and limits

This case is based on source inspection of the two applications, including the active network context and callback test setup. No integration test or live provider request was executed for this portfolio. The callback test uses a configured database and is not a standalone offline demonstration.

The customer application contains Capacitor dependencies; this is not presented as React Native experience. No station count, transaction volume or uptime metric is included.

[Back to portfolio](../../README.md)
