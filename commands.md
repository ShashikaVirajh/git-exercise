# Git Cheatsheet

This cheatsheet provides a quick reference guide for the most commonly used Git commands.

## Table of Contents

1. [Initialize Git & Manage Local Changes](#1-initialize-git--manage-local-changes)
2. [History Inspection & Comparisons](#2-history-inspection--comparisons)
3. [Branching, Merging & Stashing](#3-branching-merging--stashing)
4. [Collaboration and Remote Repositories](#4-collaboration-and-remote-repositories)
5. [Troubleshooting and Miscellaneous Commands](#5-troubleshooting-and-miscellaneous-commands)

---

## 1. Initialize Git & Manage Local Changes
This section covers commands to initialize Git, manage and view local changes.

### Clone Repository
- `git clone <url>`: Clones the repository related to `<url>`.

### Initialize Git
- `git init`: Create a new local repository.

### Stage Files
- `git add <file-name>`: Stage a single file.
- `git add .`: Stage all the files.
- `git add *.ts`: Stage all the files with a pattern.

### View the Status
- `git status`: View full status.
- `git status -s`: View short status.

### Commit Staged Files
- `git commit -m <message>`: Commit with a one-line message.
- `git commit`: Open the editor to type a long message.

### Commit By Skipping the Staging Area
- `git commit -am <message>`: Stage and commit with a single command.

### Remove Files
- `git rm <file-name>`: Remove a file from the working directory and staging area.
- `git rm --cached <file-name>`: Remove a file from the staging area only.
- After using both of these commands, changes should be committed.

### View Difference
- `git diff`: Show unstaged changes.
- `git diff --staged`: Show staged changes.

### View Commit History
- `git log`: View detailed commit history.
- `git log --oneline`: View one-line commit history.
- `git log --reverse`: View reversed commit history.
- `git log --graph --oneline`: View one-line commit history as a graph.

### View Single Commit
- `git show <commit-id>`: Show a specific commit.
- `git show HEAD`: Show the last commit.
- `git show HEAD~2`: Show two steps before the last commit.
- `git show HEAD~2:<file-name>`: Shows `<file-name>` related to 3rd latest commit.

### Unstage Files
- `git restore --staged .`: Unstage all the changes.
- `git restore --staged <file-name>`: Unstage `<file-name>`.

### Discard Local Changes
- `git restore <file-name>`: Copy file from staging to the working directory.
- `git restore .`: Copy all files from staging to the working directory.
- `git clean -fd`: Remove all untracked files (files in the working directory).

### Restore Files To An Earlier Version
- `git restore --source=HEAD~2 <file-name>`: Restore the file to 2 commits earlier.

---

## 2. History Inspection & Comparisons
This section includes commands to inspect the commit history and compare different commits.

### View The History
- `git log --stat`: Shows the list of modified files.
- `git log --patch`: Show the modified files with changes.

### Filter History
- `git log -<number>`: Shows the last `<number>` of commits. 
- `git log --author="<author-name>"`: Shows commits of `<author-name>`.
- `git log <file-name>`: Commits that are related to `<file-name>`.

### Compare Commits
- `git diff HEAD~2 HEAD`: Shows the changes between two commits.
- `git diff HEAD~2 HEAD <file-name>`: Shows the changes between two commits related to `<file-name>`.

### Display Contributors
- `git shortlog`: Shows contributors.
- `git shortlog -n`: Shows contributors and commits.
- `git shortlog -s`: Shows contributors with the number of commits.

### Display Author of Lines
- `git blame <file-name>`: Shows the author of each line in `<file-name>`.

---

## 3. Branching, Merging & Stashing
This section explains how to handle branching, merging, and stashing.

### Create New Branch
- `git branch <branch-name>`: Creates a new branch named `<branch-name>`.
- `git switch <branch-name>`: Switches to the `<branch-name>` branch.
- `git switch -c <branch-name>`: Creates and switches to `<branch-name>`.
- `git branch -D <branch-name>`: Deletes branch `<branch-name>`.

### Rename Branch
- `git branch -m <new-name>`: Rename the current branch to `<new-name>`.
- `git branch -m <old-name> <new-name>`: Rename a branch from `<old-name>` to `<new-name>`.

### Stashing
- `git stash push -m <message>`: Creates a new stash with a message.
- `git stash list`: Lists all the stashes.
- `git stash show <number>`: Shows the stash in the given index.
- `git stash apply <number>`: Applies the given stash to the working directory.
- `git stash drop <number>`: Deletes the stash in the given index.
- `git stash clear`: Deletes all the stashes.

### Merging
- `git merge <branch-name>`: Merges `<branch-name>` branch into the current branch.
- `git merge <branch-name> -m <message>`: Merges `<branch-name>` branch into the current branch with a merge commit.
- `git merge --abort`: Aborts the current merge process.

---


## 4. Collaboration and Remote Repositories
This section includes commands to manage remote repositories and collaborate with others.

### Set Up Remotes
- `git remote add <alias> <url>`: Add a remote repository with an alias.
- `git remote -v`: Lists all the remote repositories.
- `git remote rm <alias>`: Deletes the remote repository.

### Synchronize Changes
- `git fetch <alias>`: Downloads the latest changes, but does not merge.
- `git pull <alias> <branch>`: Downloads the latest changes and merges.
- `git push <alias> <branch>`: Uploads local changes to the remote.

---

## 5. Troubleshooting and Miscellaneous Commands
This section includes troubleshooting tips and miscellaneous commands.

### Find A Bug
- `git bisect start`: Starts bisecting.
- `git bisect bad`: Marks the current commit as bad.
- `git bisect good <commit>`: Marks `<commit>` as good.
- `git bisect reset`: Exits bisect mode.

### Miscellaneous Commands
- `git help <command>`: Shows the help page for `<command>`.
- `git config --global alias.<alias> <command>`: Creates an alias for `<command>`.

---

