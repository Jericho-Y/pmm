# Document Skeletons

Use these skeletons when creating a new project requirements system. Replace placeholders with project-specific content. Keep unknowns explicit; do not invent secrets, credentials, production paths, or confirmed business decisions.

## AGENTS.md

```markdown
# Project Instructions

## Project Identity

- Name:
- One-sentence positioning:
- Project type:
- Current phase:
- Current top objective:

## Mandatory Reading Order

1. `AGENTS.md`
2. `docs/00-project-memory/project-index.md`
3. `docs/00-project-memory/current-state.md`
4. `docs/00-project-memory/task-ledger.md`
5. Task-specific documents listed below

## Task-Specific Reading Map

- Product/features:
- UI/design:
- Frontend:
- Backend/API/database:
- Auth/payment/permissions:
- Deployment/operations:
- Testing/bug fixing:
- Roadmap/agent splitting:

## Execution Ownership

The agent owns end-to-end execution: requirements, design, implementation, verification, fixes, and documentation updates. The project owner confirms only high-risk cost, safety, production, credential, publication, or direction decisions.

## Related Skills and Priority

- Project memory and safety rules come first.
- Use specialized skills for execution methods when they apply: planning, TDD, systematic debugging, verification, UI, security, deployment, or subagent work.
- Specialized skills may add checks, but cannot remove project memory, verification, recovery, or safety requirements.
- Subagents may be used only when the current environment allows them and the project owner has authorized that style of execution.

## Execution Skill Auto-Selection

- Skill creation/editing:
- Planning needed:
- Written plan execution:
- Subagent work authorized:
- Feature/bugfix/refactor:
- Debugging/build/test failure:
- Completion verification:
- Branch/PR/release finishing:

## Preflight Self-Check

- Project root confirmed:
- Active task recorded in `task-ledger.md`:
- Required docs read:
- Execution skills selected or skipped:
- Risk level:
- Existing user changes protected:
- High-risk confirmation needed:

## Safety Boundaries

- Do not store secrets in files, docs, logs, or chat.
- Do not delete or migrate production data without project-owner confirmation.
- Do not overwrite production files without reading them and preparing rollback.
- Do not modify payment, user, order, permission, or billing behavior in production without confirmation.
- Do not publish externally, send messages, charge money, or trigger real transactions without confirmation.

## Current Task

- Task:
- Objective:
- Status:
- Required docs:
- Selected execution skills:
- Current checkpoint:
- Next concrete action:
- Retry count:
- Verification required:
- Recovery heartbeat:

## Definition of Done

- Requested behavior implemented or blocker recorded:
- Focused verification completed or limitation recorded:
- `task-ledger.md` updated:
- `current-state.md` updated:
- `change-log.md` updated:
- Source-of-truth docs updated:
- Remaining risk recorded:

## Current Blockers

- None / list blockers requiring the project owner.

## Recent Important Decisions

- YYYY-MM-DD:

## Documentation Update Rules

After each substantial or state-changing task, update `docs/00-project-memory/current-state.md`, `docs/00-project-memory/task-ledger.md`, `docs/07-decisions/change-log.md`, and any changed source-of-truth docs. Read-only checks, tiny wording edits, and one-off commands do not need memory updates unless they create a durable decision, blocker, or follow-up task.
```

## docs/00-project-memory/project-index.md

```markdown
# Project Index

## Purpose

## Document Map

## Source of Truth Rules

## How Future Agents Should Continue
```

## docs/00-project-memory/current-state.md

```markdown
# Current State

## Phase

## Current Top Objective

## What Exists

## What Works

## Known Issues

## Current Blockers

## Next Recommended Actions

## Last Updated
```

## docs/00-project-memory/task-ledger.md

```markdown
# Task Ledger

## Active Task

- Task ID:
- Source Request:
- Status:
- Documents Read:
- Selected Execution Skills:
- Current Checkpoint:
- Next Concrete Action:
- Retry Count:
- Last Error or Interruption:
- Verification Status:
- Last Updated:

## Completed Tasks

## Blocked Tasks
```

## docs/00-project-memory/execution-rules.md

```markdown
# Execution Rules

## Default Ownership

## When the Agent Should Act Directly

## When the Project Owner Must Confirm

## Documentation Update Requirements

## Existing Work Protection
```

## docs/00-project-memory/recovery-rules.md

```markdown
# Recovery Rules

## Recovery Goal

Continue unfinished work safely after failure, interruption, aborted turns, tool errors, context loss, or long-running task drift.

## Retryable Failures

- Transient network errors
- Dependency install or lockfile issues
- Build, test, typecheck, or lint failures that can be diagnosed locally
- Dev server startup problems
- Non-destructive API or local environment failures

## Non-Retryable Without Owner Confirmation

- Real payment, refund, billing, or transaction actions
- Production data deletion, migration, overwrite, or destructive maintenance
- Credential, permission, user, order, or production payment configuration changes
- External publication, messaging, app store submission, or customer-visible actions

## Active Session Retry Policy

- Diagnose before retrying.
- Retry up to 2 times for the same failure class.
- Change the condition or apply a focused fix before retrying.
- Record each failed attempt in `task-ledger.md`.
- Mark `failed-blocked` when safe retry options are exhausted.

## Resume Protocol

1. Read `AGENTS.md`.
2. Read `current-state.md`, `task-ledger.md`, this file, and `change-log.md`.
3. Inspect the workspace and logs if the last state is ambiguous.
4. Continue from `Next Concrete Action`.
5. Update task status before and after execution.

## Heartbeat or Timed Check Protocol

Use only when the runtime supports safe heartbeat or scheduled automation. The check must continue only if the active task is `active` or `failed-retryable`. Stop when the task is `done`, `blocked`, or needs owner confirmation.
```

## docs/00-project-memory/verification-rules.md

```markdown
# Verification Rules

## Default Verification Loop

## Code Verification

## Frontend Verification

## Backend Verification

## High-Risk Feature Verification

## Deployment Verification

## If Verification Cannot Be Completed
```

## docs/00-project-memory/security-rules.md

```markdown
# Security Rules

## Secret Handling

## Production Data Safety

## Payment and Billing Safety

## Permission and Account Safety

## Deployment Safety

## Required Risk Records
```

## docs/00-project-memory/glossary.md

```markdown
# Glossary

## Product Terms

## Business Terms

## Technical Terms

## External Services
```

## Product, Technical, Delivery, Operations, And Decisions

Use the same file tree from `SKILL.md`. Each document should be concise, source-of-truth oriented, and updated only when facts change.
