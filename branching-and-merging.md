# Git Branching and Merging

## Create New Branch

- `git branch <branch-name>`: Creates a new branch named `<branch-name>`.
- `git checkout <branch-name>`: Switches to the `<branch-name>` branch.
- `git switch <branch-name>`: Switches to the `<branch-name>` branch (newer command).
- `git checkout -b <branch-name>`: Creates and switches to `<branch-name>`.
- `git switch -c <branch-name>`: Creates and switches to `<branch-name>` (newer command).
- `git branch -D <branch-name>`: Deletes branch `<branch-name>`.

## Stashing

- `git stash push -m <message>`: Creates a new stash with a message.
- `git stash list`: Lists all the stashes.
- `git stash show <number>`: Shows the stash in the given index.
- `git stash apply <number>`: Applies the given stash to the working directory.
- `git stash drop <number>`: Deletes the stash in the given index.
- `git stash clear`: Deletes all the stashes.

## Merging

- `git merge <branch-name>`: Merges `<branch-name>` branch into the current branch.
- `git merge --no-f <branch-name>`: Creates a merge commit.
- `git merge --squash <branch-name>`: Performs a squash merge.
- `git merge --abort`: Aborts the merge.

## View Merged Branches

- `git branch --merged`: Shows the merged branches.
- `git branch --no-merged`: Shows the unmerged branches.

## Rebasing 

- `git rebase <branch-name>`: Changes the base of the current branch with origin `<branch-name>`.

## Cherry Picking

- `git cherry-pick <commit-id>`: Picks the `<commit-id>` commit into the current branch.
