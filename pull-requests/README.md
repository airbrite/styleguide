# Pull Requests

1. Create a branch with the pattern `yourname/branch-name`
1. Code
1. Create Pull Request to master
1. If the Pull Request has a Trello ticket
  * Move it to QA if has functionality to be tested by QA
  * Move it to "Done" if doesn't have functionality to be tested by QA
1. Tests must be green
1. Get at least one other developer's review and approval
  * Reviewers must leave an approval comment
1. If changes are made to the pull request after review, it needs to be reviewed again
1. Authors merge their own branches after approval and gut check


## Working with large features

1. If you encounter a feature that requires (roughly) more than two day’s work, split it into smaller tasks.
1. By all means, avoid big Pull Requests. Split your work in smaller chunks.
1. Use a single feature branch per requiered feature. If a feature requires many tasks create a branch per task and send Pull Requests against the feature branch, avoiding partials Pull Requests to master.
1. If you modify one or more components in the feature branch, create a Pull Request per component.


## Frontend

* If there are visual changes or new features, attach a screenshot
  * Before and after shots are nice
