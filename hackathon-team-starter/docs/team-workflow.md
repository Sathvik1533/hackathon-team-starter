# Team workflow

## Roles (combine for small teams)
- Product / coordinator: problem, scope, timeline, judging and submission.
- Frontend: screens, interaction states, responsive behavior and API client.
- Backend/data: API, business rules, schema, auth and storage.
- AI/integrations: model/API, prompts, retrieval/tools, evaluation and fallback.
- QA/release: tests, CI, deployment, smoke tests and demo backup.

Every deliverable has one accountable owner and a reviewer. Roles are responsibilities, not job titles.

## GitHub flow
1. Pull latest `main`.
2. Create `feature/<short-task>` or `fix/<short-task>`.
3. Make a focused change and commit with a clear message.
4. Push and open a draft PR early.
5. Describe purpose, linked issue, test steps, evidence and risks.
6. Request review; resolve comments; wait for required checks.
7. Merge using the team's agreed method.
8. Delete branch and pull updated `main`.

## Branch rules
- `main` stays demoable.
- Never force-push shared branches.
- Avoid multiple people editing high-conflict files simultaneously.
- Agree API/schema changes before frontend and backend diverge.
- Merge small changes frequently.

## Team status update
- Done:
- Next:
- Blocked:
- Need from teammate:
