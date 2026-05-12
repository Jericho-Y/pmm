# Automation

## GitHub Actions

`ci.yml` runs public safety checks on pushes and pull requests.

`daily-auto-merge.yml` runs daily and tries to merge low-risk pull requests only when:

- the pull request is not a draft
- checks pass
- changed files are in allowed paths
- no workflow, script, binary, dependency, or executable file changed
- external pull requests that change `SKILL.md` have a `safe-auto-merge` label

This keeps automation useful without allowing unreviewed changes to CI, scripts, dependencies, or executable payloads.

## Local Skill Sync

GitHub Actions cannot safely update a local machine. Use a local scheduler or agent automation to run:

```bash
bash scripts/sync-local-skill.sh
```

The script:

1. clones the public repository into a temporary directory
2. checks out `main`
3. runs public safety checks
4. backs up the existing local skill
5. syncs `SKILL.md` and `templates/`

Set these environment variables if needed:

```bash
REPO_URL=https://github.com/<owner>/project-requirements-system.git
LOCAL_SKILL_DIR=<SKILLS_ROOT>/project-requirements-system
```
