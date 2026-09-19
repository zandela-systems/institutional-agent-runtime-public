# Demo Walkthrough — Bounded Repository Execution

## Scenario

An engineering agent is asked to inspect, modify, and validate a repository.

## Governed path

### 1. Inspect
The agent begins with bounded repository inspection.

### 2. Establish candidate scope
Before mutation, an immutable ChangeSet defines exact writable paths.

### 3. Mutate only the candidate world
Changes occur in an isolated worktree rather than the canonical working tree.

### 4. Validate through fixed profiles
The model selects from runtime-owned validation profiles. It does not construct an arbitrary shell command.

### 5. Produce evidence
The runtime records stdout/stderr and an execution receipt tied to candidate and canonical Git state.

### 6. Stop before promotion
Commit, push, deploy, and canonical promotion remain outside model authority.

## Expected refusal

A request for an ungranted capability should be refused rather than improvised.

That refusal is part of the system's intended correctness, not a failure of intelligence.
