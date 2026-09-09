# Engineering Workflow

## Start with the business invariant

Before implementing a feature, I identify what must remain true: an invoice cannot be billed twice while its original operation is unresolved; a load must have one authoritative composition; a customer must only access permitted organizational data.

I translate the rule into the API contract, database operation and user-visible states. I work across the interface and backend so a partial failure does not silently become a success message.

## AI-assisted implementation

I use coding agents to help investigate code, decompose changes, implement and review. My responsibility is to decide the architecture, challenge assumptions, inspect the resulting changes and verify the behavior. Generated code is an implementation input, not evidence that a change is correct.

The number allocation case is a useful example to discuss: reproducing the old failure in an isolated database makes the correction reviewable. It is more informative than demonstrating only the successful path after a change.

## Production support

For a critical ticket, I establish user impact, identify the affected operation and trace state across the interface, database and provider boundary. I distinguish a confirmed failure from an uncertain outcome before attempting recovery.

For maintenance, I scope the change, select relevant checks, prepare a recovery path and verify the result after release. I do not describe this as a guarantee of zero regressions.

## Communication

I explain the observed behavior, the business consequence, the proposed correction and the remaining uncertainty. My event production background adds practical experience coordinating people and responding to simultaneous operational problems.

[Back to portfolio](../README.md)
