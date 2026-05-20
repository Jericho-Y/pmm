# Changelog

Purpose: Public release notes for the `pmm` skill.
Read when: Checking what changed between published versions.
Skip when: You only need internal project maintenance history.

This project follows semantic versioning for public skill releases.

## v0.1.0 - 2026-05-20

First formal public release of `pmm`.

### Added

- Durable project memory protocol built around project `AGENTS.md` plus project-local `docs/`.
- Requirements, current-state, task-ledger, decision, automation, recovery, security, and verification document skeletons.
- Agent compatibility guidance for Codex, Claude Code, Hermes, OpenCode/OpenClaw-style agents, and other `AGENTS.md`-aware agents.
- Context budget protocol for staged reading and concise durable updates.
- Source-artifact gate for PRD, requirements, screenshot, design, document, and source review tasks.
- Subagent role and ownership boundary guidance for authorized parallel agent work.
- Compact-disconnect recovery guidance and recovery-status helper.
- Public safety check for private markers, blocked file types, unexpected executables, symlinks, and documentation drift.
- Local skill sync script with destination guards, safety checks, managed-file cleanup, and local backup behavior.

### Security

- Repository-wide security scan completed with no reportable findings for the public skill repository.
