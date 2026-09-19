# IAR Authority Model — P1 to P3

Institutional Agent Runtime separates model capability from runtime authority.

## P1 — Read-only inspection

P1 is ratified. The agent may inspect repository state using bounded read/list/search/diff/log capabilities.

No mutation or command execution authority is implied.

## P2 — Isolated candidate mutation

P2 is ratified. Mutation is permitted only inside an isolated candidate worktree after an immutable ChangeSet establishes exact writable scope.

The canonical repository remains outside the mutation target.

## P3 — Controlled validation execution

P3 adds fixed validation-profile execution.

The model does **not** receive:

- arbitrary PowerShell/cmd/bash authority;
- free-form argv;
- package installation;
- Git commit;
- push;
- deployment;
- canonical promotion.

The runtime resolves fixed executables/arguments, bounds execution, and records receipts.

## Governing principle

A capable model is not automatically an authorized actor.

The runtime's job is to enforce the capability boundary and preserve evidence of what was actually allowed and executed.
