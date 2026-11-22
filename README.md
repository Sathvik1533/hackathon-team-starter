# Hackathon Team Starter

A reusable, team-first scaffold for a 24–72 hour hackathon. It provides planning templates,
GitHub workflows, team guidance and empty frontend/backend areas without forcing a technology stack.

## Start a new hackathon

1. Read [`docs/00-kickoff.md`](docs/00-kickoff.md).
2. Copy [`templates/problem-brief.md`](templates/problem-brief.md) and agree on the user, problem,
   constraints and success criteria.
3. Copy [`templates/mvp-scope.md`](templates/mvp-scope.md). Create one GitHub Issue for every
   Must-have with acceptance criteria and one accountable owner.
4. Add the app only when the team chooses a stack. Put UI code in `frontend/` and API or service
   code in `backend/`. Keep setup and test commands accurate in this README.
5. Agree on API/data contracts, then use small branches and Pull Requests.
6. Deploy a thin working slice early and reserve time for integration, testing and demo rehearsal.

## Repository structure

- `frontend/` — frontend application (currently a placeholder)
- `backend/` — backend or API application (currently a placeholder)
- `docs/` — kickoff, architecture, release and team collaboration guidance
- `templates/` — reusable planning, testing and demo documents
- `.github/ISSUE_TEMPLATE/` — issue forms for bugs and feature requests
- `.github/workflows/ci.yml` — dependency-aware CI
- `.github/PULL_REQUEST_TEMPLATE.md` — Pull Request checklist
- `CODEOWNERS.example` — optional copy to `.github/CODEOWNERS`

## Configure the applications

Copy `.env.example` to `.env` when applications need environment variables. Never commit `.env`.
Use only placeholders and local development values in this repository.

Use the README in the chosen app directories for exact commands:

- [`frontend/README.md`](frontend/README.md)
- [`backend/README.md`](backend/README.md)

The starter intentionally has no application dependencies. When one is added, update CI and README
commands to match the real stack. Do not add infrastructure or services unless a requirement needs it.

## Recommended development workflow

1. Create or select a GitHub Issue.
2. Branch from an updated `main`.
3. Make a focused commit and push the branch.
4. Open a Pull Request, link the Issue and request a review.
5. Review changes and resolve CI or merge-conflict feedback.
6. Merge only with team approval, then delete the merged branch.

See [`docs/team-workflow.md`](docs/team-workflow.md) for roles, coordination and Definition of Done.

## Run tests

This scaffold does not fake test success. CI runs only when dependency files or scripts exist:

- Frontend checks run for `frontend/package.json`; lint, test and build commands run only when
  matching package scripts exist.
- Backend checks run for `backend/requirements.txt` or `backend/pyproject.toml`; pytest runs only
  when test files or pytest configuration are present.

Document and run additional local test commands in the app READMEs. CI does not prove that a
browser test, API integration or deployment works unless the workflow explicitly runs it.

## Team Collaboration Handbook

- [Team workflow](docs/team-workflow.md)
- [Branching strategy](docs/branching-strategy.md)
- [Issue guide](docs/issue-guide.md)
- [Pull Request guide](docs/pull-request-guide.md)
- [Release checklist](docs/release-checklist.md)
- [Pull Request template](.github/PULL_REQUEST_TEMPLATE.md)
- [Bug report template](.github/ISSUE_TEMPLATE/bug-report.yml)
- [Feature request template](.github/ISSUE_TEMPLATE/feature-request.yml)
- [GitHub Actions CI](.github/workflows/ci.yml)

## Security rules

- Never commit API keys, passwords, tokens, private data or real credentials.
- Store local secrets in `.env`; store hosted secrets in the deployment or repository secret settings.
- Validate inputs and enforce authorization in the backend.
- Keep third-party permissions least-privilege and rotate exposed secrets immediately.
- Before publication, review source, logs, screenshots and generated assets for sensitive data.
