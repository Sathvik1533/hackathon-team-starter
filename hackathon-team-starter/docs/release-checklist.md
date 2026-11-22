# Release and demo checklist

## Security
- [ ] No secrets in source, logs, screenshots or chat.
- [ ] Auth and authorization enforced server-side.
- [ ] Inputs and uploads validated.
- [ ] Database and storage permissions checked.
- [ ] AI output treated as untrusted and validated.
- [ ] External integrations use least privilege.

## Release
- [ ] Clean install and production build succeed.
- [ ] Environment variables configured on host.
- [ ] Database migrations are repeatable.
- [ ] CORS, redirects, callbacks and storage URLs verified.
- [ ] Live URL tested in a clean browser session.
- [ ] Critical happy path and failure paths tested.
- [ ] Known-good commit/deployment and backup demo available.

## Submission
- [ ] Demo rehearsed on the deployed build.
- [ ] Repository, live URL, slides and forms checked.
- [ ] Sample data/test account prepared without real private data.
- [ ] Limitations stated honestly.
