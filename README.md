# Hackathon Team Starter

A reusable, team-first starting point for hackathon projects. This repository is a workflow scaffold, not a one-size-fits-all application. Keep only the tools and services required by your challenge.

## Start here
1. Read [`docs/00-kickoff.md`](docs/00-kickoff.md).
2. Copy [`templates/problem-brief.md`](templates/problem-brief.md) and agree on the user, problem, constraints and success criteria.
3. Fill [`templates/mvp-scope.md`](templates/mvp-scope.md) and create GitHub Issues for every Must-have.
4. Assign one owner per task and agree on API/data contracts before parallel coding.
5. Follow the branch → pull request → review → CI → merge workflow.
6. Deploy a thin vertical slice early. Protect the final 15–20% of the event for integration, testing, demo and submission.

## Suggested baseline (change when the problem requires it)
- Frontend: React + Vite + TypeScript
- Backend: Python + FastAPI
- Data: PostgreSQL (managed service such as Supabase when suitable)
- Tests: Vitest / Playwright / pytest
- CI: GitHub Actions

Do not add Redis, queues, vector databases, agent frameworks, Docker or cloud infrastructure unless a real requirement justifies them.

## Repository map
- `docs/` — kickoff, team workflow, architecture and release guidance
- `templates/` — problem brief, MVP scope, decision log, test plan and demo script
- `.github/` — issue/PR templates and CI workflow
- `frontend/` — placeholder for the UI application
- `backend/` — placeholder for the API application

## Local setup
This scaffold intentionally does not install application dependencies. Add the actual app after the team chooses its stack. Keep setup instructions current in this README.

## Team rules
- No direct pushes to `main` for feature work.
- One issue = one accountable owner = clear acceptance criteria.
- Small branches and small pull requests.
- Do not commit `.env`, API keys, tokens, credentials or personal data.
- CI must pass before merging where practical.
- A task is done only after review, integration and verification.

## Before making this repository public
Check that no secrets, private data, internal event material or licensed assets are present.
