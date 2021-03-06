# Git Guide

Follow the following Git steps when adding a new feature:

1. Create a new local feature branch. `git checkout -b BRANCH_NAME`
2. Commit commit commit. `git commit -m 'MESSAGE'`
3. Push local feature branch to github repository. `git push REMOTE_NAME BRANCH_NAME`
4. Create pull request to dev branch.

AFTER Code Reviews

1. Squash commits.
  * Get commit hash of last commit to not be squashed. `git log`
  * Squash. `git rebase -i COMMIT_HASH`
2. Pull remote dev branch to local dev. `git pull REMOTE_NAME dev`
3. Rebase local feature branch onto dev. `git rebase dev`
4. Push final version of local feature branch to github repository. `git push -f REMOTE_NAME BRANCH_NAME`

**Note:** DO NOT push broken code!!!