# Branching strategy

A branch is a separate line of work in Git. Branches let teammates change files without stopping
others and keep `main` in a demoable state.

## Protect `main`

For feature work, do not commit or push directly to `main`. Recommended repository settings:

- Require a Pull Request before merging.
- Require at least one approving review.
- Require CI status checks to pass.
- Prevent force-pushes and branch deletion.
- Require branches to be up to date before merge when the team can support it.

Use `main` for the latest merged, demonstrated baseline.

## Create a branch

Create a branch when a task has acceptance criteria and is ready for implementation.

```bash
git switch main
git pull --ff-only origin main
git switch -c feature/short-name
```

For bug fixes use `fix/bug-name`, docs use `docs/document-name`, and maintenance uses
`chore/task-name`. Keep names short and hyphenated.

## Commit and push

Make one logical change per commit:

```bash
git add <files>
git commit -m "Add shortlist filter"
git push -u origin feature/short-name
```

Write messages that explain what changed. Push early and open a draft Pull Request when the work can
be reviewed. Small Pull Requests merge and integrate faster.

## Synchronize with `main`

Fetch and update the branch regularly:

```bash
git fetch origin
git switch feature/short-name
git merge origin/main
```

Prefer merging `main` into a feature branch during a short hackathon. Do not rebase a branch while
other people are using it unless the team agrees.

Resolve merge conflicts by:

1. Read each conflicting file and the linked Issues or API contracts.
2. Keep the intended behavior from both sides when compatible.
3. Delete conflict markers such as `<<<<<<<`, `=======` and `>>>>>>>`.
4. Run relevant tests and review the diff.
5. Commit the conflict resolution and push again.

Never use `git push --force` on a shared branch. If history becomes severely inconsistent, stop and
ask the team coordinator or repository maintainer for help.

## Open and merge

Open a Pull Request only after the branch has a focused change and the pull-request checklist can be
completed. Follow [`pull-request-guide.md`](pull-request-guide.md).

Delete a branch after it is merged. Before deleting, confirm the PR is merged and the issue is closed.

```bash
git switch main
git pull --ff-only origin main
git branch -d feature/short-name
git push origin --delete feature/short-name
```
