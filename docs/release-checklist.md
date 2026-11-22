# Release and demo checklist

Use this checklist during the final integration and demo window. Tick items only after evidence exists.

## Feature completion

- [ ] Must-have scope is complete and acceptance criteria are demonstrated.
- [ ] No open blocker affects the demo-critical journey.
- [ ] All merged work is integrated on `main`.
- [ ] Known limitations are recorded honestly.

## Code review and CI

- [ ] Every release change has a reviewed, merged Pull Request.
- [ ] `.github/workflows/ci.yml` is running on pushes and relevant Pull Requests.
- [ ] All available CI checks pass on the release commit.
- [ ] No placeholder test or build is reported as successful without real execution.

## Frontend and backend testing

- [ ] Frontend dependencies install from a clean setup.
- [ ] Frontend build succeeds and its critical screens work.
- [ ] Backend starts successfully with documented commands.
- [ ] Automated tests cover the most important behavior.
- [ ] Responsive and keyboard paths have been manually checked.
- [ ] Error, empty, loading and offline states have been checked where applicable.

## API integration

- [ ] API request and response contracts match the frontend.
- [ ] Authentication and authorization are tested end to end.
- [ ] Critical happy and failure paths return expected results.
- [ ] CORS, callbacks and redirects work in the deployed environment.
- [ ] External APIs have fallbacks or honest demo behavior.

## Database verification

- [ ] Schema and migrations run on a clean environment.
- [ ] Seed or demo data is repeatable and contains no real private data.
- [ ] Read/write permissions are verified.
- [ ] A backup or restore path is available for the demo.

## Environment variables and secrets

- [ ] `.env.example` lists all required variable names.
- [ ] Production secrets exist only in deployment or repository secret settings.
- [ ] No secret, token or credential appears in source, logs or screenshots.
- [ ] Third-party credentials have least privilege and safe demo quotas.
- [ ] Exposed credentials have been revoked and replaced.

## Security checks

- [ ] Server-side authorization is enforced.
- [ ] Inputs, uploads and AI-generated output are validated.
- [ ] Database, storage and external-service permissions are checked.
- [ ] Dependency warnings or known critical issues have been reviewed.
- [ ] Public demo data contains no personal or confidential information.

## Deployment readiness

- [ ] Production build uses the intended environment.
- [ ] Deployment or hosting configuration is saved and documented.
- [ ] Health and smoke endpoints work.
- [ ] Live URL opens on a clean browser session.
- [ ] A known-good commit and deployment URL are recorded.

## Production smoke testing

- [ ] Open the deployed app and complete the primary demo journey.
- [ ] Test one rejection or error path.
- [ ] Verify reload and navigation behavior.
- [ ] Check browser console and server logs for unexpected errors.
- [ ] Confirm the system works on presentation hardware/network.

## Demo preparation

- [ ] Demo script follows the main user journey.
- [ ] Screenshots and backup media are available.
- [ ] Sample account and demo data are ready.
- [ ] Team members know handoff and failure-recovery roles.
- [ ] A local or recorded backup works without external network dependencies.

## Final presentation

- [ ] Repository, live URL, slides and submission form are accessible.
- [ ] Presenter and timing are assigned.
- [ ] Limitations and future work are stated clearly.
- [ ] Submission deadline has been checked in the event timezone.

## Post-hackathon cleanup

- [ ] Rotate any shared temporary credentials.
- [ ] Remove accidental production data or test accounts.
- [ ] Close or document unresolved Issues.
- [ ] Record useful decisions and next steps.
