# GitHub Repository And Project Backlog Runbook

Use this when creating or maintaining the GitHub repository and GitHub Projects backlog.

## Preconditions

- `gh auth status` must show an authenticated GitHub account.
- `gh project` requires the `project` OAuth scope.
- If missing, run `gh auth refresh -s project`.

## Repository Setup

1. Confirm local git state with `git status --short --branch`.
2. Add or update durable project files such as `README.md`, `decisions.jsonl`, and runbooks.
3. Commit the initial project setup.
4. Create the GitHub repository with `gh repo create`.
5. Push `main` and set the upstream.

## Backlog Setup

1. Create labels for area, type, priority, and phase.
2. Create an MVP milestone.
3. Create focused issues for product slices, not implementation trivia.
4. Create a GitHub Project for the backlog.
5. Link the project to the repository.
6. Add created issues to the project.
7. Keep large architectural choices recorded in `decisions.jsonl`.

## Current Backlog Themes

- Convex app foundation.
- Title search and work normalization.
- User list/status/review tracking.
- Source record and platform link caching.
- Background enrichment jobs.
- OpenRouter LLM batch analysis.
- Taste profile aggregation.
- Recommendation batch generation.
- Privacy and data export.
