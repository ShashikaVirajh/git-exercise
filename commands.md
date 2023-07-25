# Initialize Git & Manage Local Changes

## Initialize Git
- `git init`: Create a new local repository.

## Stage Files
- `git add <file-name>`: Stage a single file.
- `git add .`: Stage multiple files.
- `git add *.ts`: Stage files with a pattern.

## View the Status
- `git status`: View full status.
- `git status -s`: View short status.

## Commit Staged Files
- `git commit -m <message>`: Commit with a one-line message.
- `git commit`: Open the editor to type a long message.

## Commit By Skipping the Staging Area
- `git commit -am <message>`: Stage and commit with a single command.

## Remove Files
- `git rm <file-name>`: Remove a file from the working directory and staging area.
- `git rm --cached <file-name>`: Remove a file from the staging area only.
- After using both of these commands, changes should be committed.

## View Difference
- `git diff`: Show unstaged changes.
- `git diff --staged`: Show staged changes.

## View Commit History
- `git log`: View detailed commit history.
- `git log --oneline`: View one-line commit history.
- `git log --reverse`: View reversed commit history.

## View Single Commit
- `git show <commit-id>`: Show a specific commit.
- `git show HEAD`: Show the last commit.
- `git show HEAD~2`: Show two steps before the last commit.
- `git show HEAD~2:<file-name>`: Shows `<file-name>` related to 3rd latest commit.

## Unstage Files
- `git restore --staged .`: Unstage all the changes.
- `git restore --staged customer.ts`: Unstage `customer.ts`.

## Discard Local Changes
- `git restore <file-name>`: Copy file from staging to the working directory.
- `git restore .`: Copy all files from staging to the working directory.
- `git clean -fd`: Remove all untracked files (files in the working directory).

## Restore Files To An Earlier Version
- `git restore --source=HEAD~2 <file-name>`: Restore the file to 2 commits earlier.


# History Inspection & Comparisons

## View The History
- `git log --stat`: Shows the list of modified files.
- `git log --patch`: Show the modified files with changes.

## Filter History
- `git log -<number>`: Shows the last `<number>` of commits. 
- `git log --author="<author-name>"`: Shows commits of `<author-name>`.
- `git log <file-name>`: Commits that are related to `<file-name>`.
- 
## Compare Commits
- `git diff HEAD~2 HEAD`: Shows the changes between two commits.
- `git diff HEAD~2 HEAD <file-name>`: Shows the changes between two commits related to `<file-name>`.

## Display Contributors
- `git shortlog`: Shows contributors.
- `git shortlog -n`: Shows contributors and commits.
- `git shortlog -s`: Shows contributors with the number of commits.

## Display Author of Lines
- `git blame <file-name>`: Shows the author of each line in `<file-name>`.


# Branching, Merging & Stashing

## Create New Branch
- `git branch <branch-name>`: Creates a new branch named `<branch-name>`.
- `git switch <branch-name>`: Switches to the `<branch-name>` branch.
- `git switch -c <branch-name>`: Creates and switches to `<branch-name>`.
- `git branch -D <branch-name>`: Deletes branch <branch-name>.

## Rename Branch
- `git branch -m <new-name>`: Rename the current branch to <new-name>.
- `git branch -m <old-name> <new-name>`: Rename a branch from <old-name> to <new-name>.

## Stashing
- `git stash push -m <message>`: Creates a new stash with a message.
- `git stash list`: Lists all the stashes.
- `git stash show <number>`: Shows the stash in the given index.
- `git stash apply <number>`: Applies the given stash to the working directory.
- `git stash drop <number>`: Deletes the stash in the given index.
- `git stash clear`: Deletes all the stashes.

## Merging
- `git merge <branch-name>`: Merges `<branch-name>` branch into the current branch.
- `git merge --no-ff <branch-name>`: Creates a merge commit.
- `git merge --squash <branch-name>`: Performs a squash merge.
- `git merge --abort`: Aborts the merge.

## View Merged Branches
- `git branch --merged`: Shows the merged branches.
- `git branch --no-merged`: Shows the unmerged branches.

## Rebasing 
- `git rebase <branch-name>`: Changes the base of the current branch with origin `<branch-name>`.
- `git rebase --abort`: Abort the rebase.
- `git rebase --continue`: Continue the rebase after resolving conflicts.

## Cherry Picking
- `git cherry-pick <commit-id>`: Picks the `<commit-id>` commit into the current branch.
- `git cherry-pick --continue`: Continue cherry-pick after resolving conflicts.


# Collaboration and Remote Repositories

## Clone Repository
- `git clone <url>`: Clones the repository related to `<url>`.

## Sync With Remote
- `git fetch origin <branch-name>`: Fetches `<branch-name>` branch from origin.
- `git fetch` or `git fetch origin`: Fetches all commits from origin.
- `git pull`: Fetch origin + merge.
- `git push` or `git push origin <branch-name>`: Pushes local `<branch-name>` to origin.

## Sharing Branches
- `git branch -r`: Shows remote tracking branches.
- `git branch -vv`: Shows local and remote tracking branches.
- `git push -u origin <branch-name>`: Pushes `<branch-name>` to origin.
- `git push -d origin <branch-name>`: Deletes `<branch-name>` from origin.

## Manage Remotes
- `git remote`: Shows remote repositories.
- `git remote add <remote-name> url`: Adds a new remote called `<remote-name>`.
- `git remote rm <remote-name>`: Deletes remote `<remote-name>`.


# Troubleshooting and Miscellaneous Commands

- `git reset --hard HEAD`: Discards all local changes and resets to the latest commit.
- `git reflog`: Shows a list of all actions performed in the repository.
- `git bisect`: Used to find commits that introduce bugs
- `git grep <text>`: Searches through the application source code.
