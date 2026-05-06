# ci-repo

Public CI proxy for a private iOS repo.

## How it works

This repo contains no source code — only GitHub Actions workflows that run CI/CD on behalf of a private repo.

1. **Private repo** pushes/PRs trigger lightweight dispatch workflows
2. Those workflows send `repository_dispatch` events to this public repo
3. **This repo** clones the private source (via `PRIVATE_REPO_PAT` + `PRIVATE_REPO` secrets), builds, tests, and reports status bac

> **No source code is stored in this repo.** It is cloned at runtime and deleted after each run.
