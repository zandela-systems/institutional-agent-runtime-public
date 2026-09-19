# IAR Evidence Summary

This summary is derived from the private canonical `CURRENT.yaml` and build history.

## P1 — RATIFIED

- Read-only conversational vertical slice
- Windows target validation: PASS
- Live OpenAI read-only smoke: PASS

## P2 — RATIFIED

- Isolated Mutation Engine
- Deterministic build validation: PASS
- Windows target validation: PASS
- Live OpenAI mutation smoke: PASS
- ChangeSet-before-mutation provenance: PASS

## P3 — implemented, not yet ratified in the referenced canonical state

Recorded evidence includes:

- implementation complete;
- 54 local deterministic tests PASS;
- Windows target validation PASS after REM-001;
- live OpenAI validation smoke PASS;
- producer adversarial review: CONDITIONAL PASS;
- fresh independent review: PENDING in the referenced state.

## Authority state

The same canonical state records:

- mutation authority: candidate-worktree ChangeSet only;
- validation execution authority: fixed profile catalog only;
- arbitrary shell authority: NONE;
- commit authority: NONE;
- push authority: NONE;
- promotion authority: NONE.

## Scope

This is an evidence summary, not a claim that P3 has been human-ratified or that the native host is an OS/network sandbox.
