# ci-repo

Public CI proxy for a private iOS repo.

## How it works

This repo contains no source code — only GitHub Actions workflows that run CI/CD on behalf of a private repo.

1. **Private repo** pushes/PRs trigger lightweight dispatch workflows
2. Those workflows send `repository_dispatch` events to this public repo
