# Contributing

## Branching & PRs
- Trunk-based: branch from `master`, small PRs, merge early.
- Name branches like `feature/ABC-123-short-title` or `fix/short-title`.
- Always open a PR; direct pushes to `master` and `release/*` are blocked.

## Commit messages
- Follow **Conventional Commits** (`feat:`, `fix:`, `docs:`, `chore:`, `refactor:`).
- Reference an issue ID when applicable.

## Reviews
- At least **2 approvals** on `master`, **1–2** on `release/*` including CODEOWNERS.
- CI must be green; resolve all comments.

## Releases & LTS
- New releases are created from `master` by annotated, signed tags `vX.Y.Z`.
- Backports land on `release/X.Y` via cherry-pick PRs and are re-tagged `vX.Y.Z+1`.
