# Fork maintenance (`ababber/spec-kit`)

This repository is a **public mirror** of [github/spec-kit](https://github.com/github/spec-kit). Keep commits publishable.

## Do not commit here

| Item | Where it belongs |
|------|------------------|
| `.route-cursor` with kit/shadow navigation | Private **`ababber/shadow-spec-kit`** |
| Shadow-architecture, trust, focus, `ckexpand` vocabulary | **`ababber/shadow-spec-kit`** |
| QC factory SDD (`specs/`, `.specify/`) | **`ababber/shadow-quant-connect`** |

## Pre-commit guard (required)

```bash
git config core.hooksPath .githooks
chmod +x .githooks/pre-commit
```

Or from the kit workspace:

```bash
ababber/shadow-spec-kit/install-publishable-hooks.sh
```

Commits that stage forbidden paths or phrases are **blocked** unless `SKIPPUBLISHABLEGUARD=1` (emergency only).

## Upstream sync

```bash
git fetch upstream --prune
git merge upstream/main
git push origin main
```

Internal workflow: **`ababber/shadow-spec-kit/SHADOW-SPEC-KIT-WORKFLOW.md`**.
