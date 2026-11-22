# Team workflow

This guide describes a practical process for a 24–72 hour team. Keep one shared source of truth,
assign every task an owner, and prefer small, frequent integrations.

## Plan the work

1. Read the hackathon rules and judging criteria.
2. Use [`00-kickoff.md`](00-kickoff.md) to agree on the user, problem, MVP and deadline.
3. Break the MVP into Issues small enough to complete in a few hours.
4. Write acceptance criteria that can be demonstrated.
5. Mark dependencies and assign one accountable owner per Issue.
6. Add a reviewer for each workstream before coding starts.

An Issue can be large for an MVP feature, but it should not hide several independent changes.

## Use GitHub Projects

Create a Project board with these columns:

| Column | Meaning |
| --- | --- |
| Backlog | Valid task, not ready to start |
| Ready | Scoped, assigned and unblocked |
| In Progress | One owner is actively working |
| In Review | A Pull Request exists and review is requested |
| Done | Accepted, merged and integrated |

Move an Issue only as the actual work changes. A Pull Request does not move work to Done until it is
merged and verified. Set Priority, Workstream Category and Due date fields if the team creates them.

## Responsibilities

Roles describe responsibilities, not exclusive ownership:

- **Coordinator/Product:** scope, priorities, board, judging criteria and submission.
- **Frontend:** screens, states, accessibility and API consumption.
- **Backend/Data:** APIs, validation, schema, authorization and storage.
- **Integrations/QA:** external services, test cases, CI, deployment and smoke testing.

Combine roles for a small team. Every deliverable has an owner and a reviewer.

## Daily coordination

Hold a 10-minute sync at the start of each work block:

- Done: what was merged or verified
- Next: what is the next 2–4 hour goal
- Blocked: what is waiting
- Need: which person or decision is needed

Keep decisions and links in Issues or team chat; do not distribute requirements only through a call.
Post one async summary if a teammate cannot attend.

## Issue assignment

Assign the person most able to complete the task, not whoever is immediately available. Only assign
one owner. Add reviewers or collaborators in the Issue, or in a comment. Do not leave Ready work
unowned. If a team member changes work, explicitly reassign the Issue and update the board.

Create Issues for bug reports, feature requests and discrete tasks. Use
[`issue-guide.md`](issue-guide.md) for writing and labels.

## Blockers and conflicts

Post the blocker in the team channel and link the Issue. State:

1. what is blocked;
2. what is needed;
3. the owner of the next decision;
4. the deadline or impact.

Agree on API, data and UI contracts before parallel implementation. If a technical conflict has a
cost, the owner proposes a short option comparison and the coordinator or relevant leads decide.
Escalate unresolved decisions quickly rather than creating incompatible work.

## Definition of Done

A task is Done only when:

- [ ] Acceptance criteria are demonstrated.
- [ ] The Pull Request is reviewed and approved.
- [ ] Required CI checks pass or are explicitly unavailable.
- [ ] The change is merged into `main`.
- [ ] Relevant integration and manual tests pass.
- [ ] Setup documentation or environment examples are updated.
- [ ] No secrets or private data were added.
- [ ] The team can explain the result in the demo.

## Four-person example

For a 48-hour hackathon:

- **Alex (Coordinator):** owns the problem brief, MVP scope, board and submission.
- **Blair (Frontend):** owns routes, UI states, accessibility and demo screens.
- **Casey (Backend):** owns API contracts, validation, database and authorization.
- **Dev (QA/Integrations):** owns CI, external integrations, test evidence and deployment.

Alex and Casey agree the API contract. Blair and Casey update a shared contract issue together.
Dev merges only after checks and smoke tests. Each feature Issue has one owner and a different reviewer.
