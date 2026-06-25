# Merge Conflict Playbook

Use this playbook when a Meridian documentation or governance pull request reports merge conflicts.

## Immediate Checks

1. Confirm the working tree is clean before starting conflict resolution.
2. Update from the target branch.
3. Search for conflict markers before committing.
4. Re-run Markdown link and required-file validation after resolving conflicts.

## Resolution Principles

- Preserve privacy and regulated-boundary language unless a reviewer explicitly approves a change.
- Prefer the most complete governance artifact when two branches edit the same documentation area.
- Keep repository index links synchronized across `README.md`, `docs/README.md`, and `profile/README.md`.
- Do not delete security, privacy, support, contribution, issue-template, or PR-template files to make a conflict easier.
- Do not introduce real client, caller, patient, transcript, credential, or operationally sensitive data while resolving examples.

## Common Conflict Areas

| File or area | Resolution guidance |
| --- | --- |
| `README.md` | Keep the direct repository index so changes remain visible when viewing the repo. |
| `profile/README.md` | Keep Meridian positioning, operating principles, and links to all public governance artifacts. |
| `docs/README.md` | Keep the documentation index synchronized with all docs currently present in `docs/`. |
| `.github/ISSUE_TEMPLATE/*` | Keep privacy confirmations and warnings that prevent sensitive disclosures. |
| `.github/PULL_REQUEST_TEMPLATE.md` | Keep risk, privacy, validation, and reviewer sections. |
| `SECURITY.md` | Keep vulnerability reporting guidance and public-repository data boundaries. |

## Required Post-Resolution Validation

Run these checks before committing a conflict resolution:

```bash
rg -n "^(<<<<<<<|=======|>>>>>>>)" .
```

```bash
git diff --check
```

```bash
python3 - <<'PY'
from pathlib import Path
required = [
    'README.md', 'profile/README.md', 'docs/README.md',
    'CONTRIBUTING.md', 'SECURITY.md', 'SUPPORT.md', 'CODE_OF_CONDUCT.md',
    '.github/PULL_REQUEST_TEMPLATE.md', '.github/ISSUE_TEMPLATE/config.yml',
]
for f in required:
    p = Path(f)
    if not p.exists():
        raise SystemExit(f'Missing {f}')
    if not p.read_text(encoding='utf-8').strip():
        raise SystemExit(f'Empty {f}')
print('Required conflict-resolution files are present and non-empty')
PY
```

## Commit Message Guidance

Use a direct message such as:

```text
Resolve documentation merge conflicts
```

The pull request description should mention the conflicted files, the resolution strategy, and the validation commands that passed.
