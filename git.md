# Git Guide

## Feature Branches

When working on features, always create a feature branch off of `master`.

Example feature branch name: `yourname/feature-name`

## Pull Requests

When a feature branch is ready to be merged into `master`,
a pull request should be created from the feature branch into the master branch.

At least one other engineer on the team must approve the PR before it can be merged.
For example, one might comment `LGTM` (looks good to me).

### Visual Changes

If there are visual changes, attach a screenshot.
Before and after shots are a bonus.

### Bumping Dependencies (npm)

Link to the CHANGELOG, HISTORY, or COMMITS for each dependency on Github.

Example for lodash: `https://github.com/lodash/lodash/wiki/Changelog`

### Other Notes

- Automated unit tests on Github must pass.
- Authors merge their own PRs after approval.
- Anything merged into `master` **can and will** be deployed to production at any time.

## Rewriting Git History

If the git commit history of a feature branch gets messy,
it is a good idea to consider rewriting the history.

To do this, you can first choose how far back you want to rewrite by findng the
commit sha of the commit you want to rewrite up until

For example, if your history has the following 5 commits...

```
commit 5
commit 4
commit 3
commit 2
commit 1
```

And you want to rewrite the history of 3 to 5, run `git reset 2`.

Your history will now be...

```
commit 2
commit 1
```

Anything that was previously committed in 3, 4, or 5 are now uncommitted changes.

## Dealing with Pull Conflicts

Sometimes when trying to pull a remote branch to an existing local branch, the remote branch may have been rebased and requires a hard (force) reset.

```
git reset --hard origin/branch/name
```
