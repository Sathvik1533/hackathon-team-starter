# Issue guide

GitHub Issues are short records of work, defects or decisions. They give the team an owner,
acceptance criteria, discussion history and a link to the resulting Pull Request.

## When to create an Issue

Create an Issue when a task needs:

- visible ownership;
- acceptance criteria;
- design or API discussion;
- work to appear on the Project board;
- a link from a Pull Request.

Use a feature request for user-visible capability, a bug report for broken expected behavior, and
a task Issue for integration, testing, documentation or release work.

Reuse the templates under [`.github/ISSUE_TEMPLATE/`](../.github/ISSUE_TEMPLATE/).

## Write a clear title

Use the outcome and affected area:

- `Add saved search to dashboard`
- `Fix empty-state crash after sign-in`
- `Configure production API environment variables`

Avoid vague titles such as `Fix frontend`, `Help`, or `It doesn't work`.

## Describe requirements

A useful Issue contains:

- the problem or desired outcome;
- the target user or affected component;
- acceptance criteria;
- dependencies;
- expected test evidence;
- links to designs or API contracts;
- no private data or credentials.

Write acceptance criteria as testable statements:

```text
Given I am signed out,
when I open the dashboard,
then I am redirected to the sign-in page.
```

## Assign and track work

1. Assign one accountable owner.
2. Add a reviewer or teammate who can unblock the work.
3. Add the Issue to the team GitHub Project.
4. Set Priority and Workstream Category fields if the project uses them.
5. Set a due date only when it communicates a real deadline.
6. Move it between Backlog, Ready, In Progress, In Review and Done as work changes.

Do not assign multiple people as the single owner. Link a shared sub-task if one feature has
independent pieces.

## Link Issues to Pull Requests

In the Pull Request description, use:

```text
Closes #123
```

GitHub closes the Issue after merge if the Pull Request targets the expected branch. Use
`Refs #123` when the Pull Request is related but should not close the Issue.

When work is larger than one Pull Request, each PR should link the Issue and explain what remains.
