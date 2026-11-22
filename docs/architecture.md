# Architecture decision guide

Start with the simplest architecture that satisfies the challenge.

## Decide
- What is the main user journey?
- Which data must persist?
- Which operations must be protected by the backend?
- Is an external API/model genuinely central to the value?
- Are background jobs, real-time updates or file storage actually required?

## Default profile (optional)
React/Vite UI → FastAPI API → PostgreSQL.
Add object storage for files, model APIs for AI features, queues for slow/retryable work, and vector search for retrieval only when requirements justify them.

## API contract
For each endpoint document:
- Method and path
- Purpose and owner
- Auth requirement
- Request schema
- Response schema
- Validation and status codes
- Error response
- Example request/response
- Idempotency / retry behavior for writes

## Architecture decision record
Use `templates/decision-log.md`. Record alternatives and why they were deferred.
