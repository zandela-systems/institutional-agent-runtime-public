# Institutional Agent Runtime

**Governed agent execution under explicit authority boundaries, deterministic validation, refusal, evidence, and human control.**

Institutional Agent Runtime (IAR) explores a question that becomes more important as AI systems gain execution capability:

> **What should an agent be allowed to do, under whose authority, against what state, and with what evidence afterward?**

## What IAR is

IAR is a governed agent runtime.

Its architectural responsibility is **execution**: models can reason and propose actions, while the runtime determines what capabilities actually exist and whether a requested action is authorized.

The current engineering program uses Git repositories as a proving ground for progressively bounded capability.

## What has been demonstrated

### Read-only inspection
The agent can inspect repository state without mutation authority.

### Isolated candidate mutation
Changes occur inside an isolated candidate worktree rather than silently modifying canonical state.

An immutable ChangeSet establishes the writable scope before mutation.

### Controlled validation execution
Validation capabilities are selected from runtime-owned profiles rather than exposing arbitrary shell or free-form command execution.

Execution produces receipts tied to candidate and canonical state.

## Authority boundary

The current design deliberately excludes implicit authority for:

- arbitrary shell execution;
- unrestricted argv/command construction;
- package installation;
- Git commit;
- push;
- deployment;
- canonical promotion.

A capable model is not automatically an authorized actor.

When a request falls outside the runtime's granted capability, the correct behavior is to **refuse, preserve state, and return evidence of the boundary encountered**.

## Operating model

```text
human authority
→ bounded capability grant
→ model reasoning
→ runtime enforcement
→ candidate action
→ deterministic validation
→ execution receipt
→ review
→ human promotion
```

## Why this matters

AI execution becomes safer and more credible when capability and authority are treated as separate things.

IAR is designed around that separation:

- the model can be intelligent without being authoritative;
- execution can be fast without becoming unbounded;
- failure can be recorded without contaminating canonical state;
- promotion remains explicit and reviewable.

## Public boundary

This repository is a curated public projection of a private canonical engineering repository.

It omits credentials, private evidence, raw prompts, internal traces, and implementation details that are not intended for publication.

## Related systems

- [ZANDELA / LIVING SYSTEM](https://github.com/zandela-systems/zandela-living-system-public)
- [ZANDELA Proof Engine](https://github.com/zandela-systems/zandela-proof-engine-public)
- [zandela.systems](https://zandela.systems)

## Status

The public showcase reflects a narrower evidence-backed claim than the full architecture by design.

---

**Capability can scale. Authority should remain explicit.**
