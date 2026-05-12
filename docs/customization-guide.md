# Customization Guide

## Project Roots

Replace `<PROJECTS_ROOT>` with your own project workspace. Keep temporary files in a dedicated temp folder so generated artifacts do not mix with source code and documentation.

## Skills Root

Replace `<SKILLS_ROOT>` with your local agent skill directory. The exact path depends on your agent runtime.

## Server Inventory

Use `templates/server-inventory.example.md` only as a shape reference. Keep real server inventories private and ignored by Git.

## Execution Skills

If your agent supports specialized skills, connect them through the decision table in `SKILL.md`. If it does not, keep the project memory, verification, and recovery rules and skip unavailable integrations.

## Project Owner Confirmation

Customize high-risk confirmation boundaries for your organization. Do not remove confirmation for production data, payment, credentials, external publication, or customer-visible actions unless you have a separate safety control.
