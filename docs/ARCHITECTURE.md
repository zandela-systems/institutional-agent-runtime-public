# Public Architecture

Institutional Agent Runtime separates **model reasoning** from **runtime authority**.

## Core flow

```text
human authority
→ bounded capability
→ model proposal
→ runtime enforcement
→ isolated candidate action
→ deterministic validation
→ execution receipt
→ review
→ human promotion
```

## Key boundaries

- canonical state is not mutated implicitly;
- writable scope is established before mutation;
- validation capabilities are runtime-owned;
- arbitrary shell is not assumed;
- promotion authority remains external to the model.

## Public boundary

This overview omits sensitive implementation details, secrets, internal traces, and unpublished security mechanics.
