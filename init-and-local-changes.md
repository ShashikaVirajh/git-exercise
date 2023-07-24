# Git Initialization and Local Changes

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
- `git show HEAD:customer.ts`: Show the version of customer.ts of the last commit.

## Unstage Files

- `git restore --staged .`: Unstage all the changes.
- `git restore --staged customer.ts`: Unstage `customer.ts`.

## Discard Local Changes

- `git restore <file-name>`: Copy file from staging to the working directory.
- `git restore .`: Copy all files from staging to the working directory.
- `git clean -fd`: Remove all untracked files (files in the working directory).

## Restore Files To An Earlier Version

- `git restore --source=HEAD~2 <file-name>`: Restore the file to 3 commits earlier.
