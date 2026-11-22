# Pull Request guide

A Pull Request (PR) proposes merging a branch into another branch. It is a review and integration
tool, not only a merge button.

## Before opening a PR

Open the PR when:

- the work satisfies or materially demonstrates the Issue's acceptance criteria;
- local checks and relevant tests have been run;
- the diff is reasonably focused;
- setup or environment changes are documented;
- no secrets or private data are included.

For an unfinished but reviewable design, open a draft PR and mark it ready for review only when it
is safe to merge.

## Select branches

- **base**: the branch receiving the change, normally `main`;
- **compare**: the feature, fix, docs or chore branch containing the change.

Confirm the target is `main` and compare it with the correct branch. Keep the PR separate from
unrelated work.

## Write the PR

Use a short title that describes the outcome, for example `Add saved search filter`.

Use [the repository Pull Request template](../.github/PULL_REQUEST_TEMPLATE.md). Describe:

- what changed and why;
- `Closes #issue-number` for the main Issue;
- commands run and manual verification;
- screenshots or demo evidence;
- known limitations or risks.

The description should let a teammate review the change without asking for basic context.

## Request and conduct review

Request at least one reviewer who understands the area. Reviewers should inspect:

- acceptance criteria and expected behavior;
- correctness and edge cases;
- security, data handling and secrets;
- tests and CI evidence;
- documentation and deployment impact;
- small, understandable diff size.

Review comments should identify the relevant behavior or code and suggest a concrete resolution.
Prefer approval or request changes through GitHub instead of informal disagreement in chat.

## Resolve review comments

The PR author should:

1. respond to each comment;
2. make a focused correction or explain why the requested change is not appropriate;
3. run checks again;
4. push the new commits;
5. re-request review after substantive changes.

The reviewer should recheck changed behavior and mark resolved comments only after resolution.

## Approvals and merge readiness

Do not merge while:

- required reviewers have requested changes;
- CI has failing required checks;
- merge conflicts remain;
- acceptance criteria are unmet;
- secret or privacy issues remain unresolved.

If a blocking review cannot finish before the deadline, document the risk, merge only under an
explicit team decision, and create a follow-up Issue. Do not bypass repository protection silently.

## Choose a merge method

Ask the team to set one default:

- **Squash and merge:** combines the PR into one commit; useful for a readable `main` and small
  hackathon PRs.
- **Merge commit:** preserves the branch commit history; useful when commits are independently
  meaningful.
- **Rebase and merge:** creates linear history but rewrites individual commit identities.

For most beginner hackathon teams, squash merge is the simplest default.

After merge:

1. Confirm the linked Issue is closed.
2. Delete the merged branch.
3. Pull updated `main` locally.
4. Remove the branch from the board once verification is complete.
