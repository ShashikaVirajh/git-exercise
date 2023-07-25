# 🚀 Git Cheatsheet

> This cheatsheet provides a quick reference guide for the most commonly used Git commands. Happy coding! 👨‍💻

## 📚 Table of Contents

1. [Initialize Git & Manage Local Changes](#initialize-git--manage-local-changes)
2. [History Inspection & Comparisons](#history-inspection--comparisons)
3. [Branching, Merging & Stashing](#branching-merging--stashing)
4. [Collaboration and Remote Repositories](#collaboration-and-remote-repositories)
5. [Troubleshooting and Miscellaneous Commands](#troubleshooting-and-miscellaneous-commands)


---

## 1. 🏁 Initialize Git & Manage Local Changes

> This section covers commands to initialize Git, manage and view local changes.

# Clone Repository
git clone <url> # Clones the repository related to <url>

# Initialize Git
git init # Create a new local repository

# Stage Files
git add <file-name> # Stage a single file
git add . # Stage all the files
git add *.ts # Stage all the files with a pattern

# View the Status
git status # View full status
git status -s # View short status

# Commit Staged Files
git commit -m <message> # Commit with a one-line message
git commit # Open the editor to type a long message

# Commit By Skipping the Staging Area
git commit -am <message> # Stage and commit with a single command

# Remove Files
git rm <file-name> # Remove a file from the working directory and staging area
git rm --cached <file-name> # Remove a file from the staging area only

# View Difference
git diff # Show unstaged changes
git diff --staged # Show staged changes

# View Commit History
git log # View detailed commit history
git log --oneline # View one-line commit history
git log --reverse # View reversed commit history
git log --graph --oneline # View one-line commit history as a graph

# View Single Commit
git show <commit-id> # Show a specific commit
git show HEAD # Show the last commit
git show HEAD~2 # Show two steps before the last commit
git show HEAD~2:<file-name> # Shows <file-name> related to 3rd latest commit

# Unstage Files
git restore --staged . # Unstage all the changes
git restore --staged customer.ts # Unstage customer.ts

# Discard Local Changes
git restore <file-name> # Copy file from staging to the working directory
git restore . # Copy all files from staging to the working directory
git clean -fd # Remove all untracked files (files in the working directory)

# Restore Files To An Earlier Version
git restore --source=HEAD~2 <file-name> # Restore the file to 2 commits earlier


## 2. 🕵️‍♂️ History Inspection & Comparisons

> This section includes commands to inspect the commit history and compare different commits.

# View The History
git log --stat # Shows the list of modified files
git log --patch # Show the modified files with changes

# Filter History
git log -<number> # Shows the last <number> of commits
git log --author="<author-name>" # Shows commits of <author-name>
git log <file-name> # Commits that are related to <file-name>

# Compare Commits
git diff HEAD~2 HEAD # Shows the changes between two commits
git diff HEAD~2 HEAD <file-name> # Shows the changes between two commits related to <file-name>

# Display Contributors
git shortlog # Shows contributors
git shortlog -n # Shows contributors and commits
git shortlog -s # Shows contributors with the number of commits

# Display Author of Lines
git blame <file-name> # Shows the author of each line in <file-name>

3. 🌴 Branching, Merging & Stashing
   
> This section explains how to handle branching, merging, and stashing.

# Create New Branch
git branch <branch-name> # Creates a new branch named <branch-name>
git switch <branch-name> # Switches to the <branch-name> branch
git switch -c <branch-name> # Creates and switches to <branch-name>
git branch -D <branch-name> # Deletes branch <branch-name>

# Rename Branch
git branch -m <new-name> # Rename the current branch to <new-name>
git branch -m <old-name> <new-name> # Rename a branch from <old-name> to <new-name>

# Stashing
git stash push -m <message> # Creates a new stash with a message
git stash list # Lists all the stashes
git stash show <number> # Shows the stash in the given index
git stash apply <number> # Applies the given stash to the working directory
git stash drop <number> # Deletes the stash in the given index
git stash clear # Deletes all the stashes

# Merging
git merge <branch-name> # Merges <branch-name> branch into the current branch
git merge --no-ff <branch-name> # Creates a merge commit
git merge --squash <branch-name> # Performs a squash merge
git merge --abort # Aborts the merge

# View Merged Branches
git branch --merged # Shows the merged branches
git branch --no-merged # Shows the unmerged branches

# Rebasing
git rebase <branch-name> # Performs an interactive rebase
git rebase --continue # Continues the rebase after resolving conflicts
git rebase --abort # Aborts the rebase

4. 🤝 Collaboration and Remote Repositories

> This section includes commands to manage remote repositories and collaborate with others.

# Add Remote Repository
git remote add <name> <url> # Add a new remote repository
git remote -v # List all remote repositories
git remote remove <name> # Removes a remote repository

# Fetch Data From Remote Repository
git fetch <name> # Fetches data from a remote repository

# Pull Changes
git pull <name> <branch-name> # Pulls changes from a remote branch
git pull --rebase <name> <branch-name> # Performs a rebase instead of a merge

# Push Changes
git push <name> <branch-name> # Pushes changes to a remote branch
git push <name> --delete <branch-name> # Deletes a remote branch

# Tracking Branches
git branch -u <name>/<branch-name> # Sets an upstream branch
git branch -vv # Shows tracking branches

# Tagging
git tag <tag-name> # Creates a lightweight tag
git tag -a <tag-name> # Creates an annotated tag
git push <name> <tag-name> # Pushes a tag
git push <name> --tags # Pushes all tags

5. 🔧 Troubleshooting and Miscellaneous Commands

> This section includes a set of helpful troubleshooting commands and some miscellaneous Git commands.

# Cherry-Picking
git cherry-pick <commit-id> # Applies the changes from a specific commit to the current branch

# Sign a Commit
git commit -S # Sign a commit
git log --show-signature # Show signed commits

# Miscellaneous Commands
git help <command> # Show help for a git command
git config --global user.name "<your-name>" # Set your username
git config --global user.email "<your-email>" # Set your email

# Troubleshooting Commands
git bisect start # Start bisecting
git bisect good <commit-id> # Mark a commit as good
git bisect bad <commit-id> # Mark a commit as bad
git bisect reset # Reset bisect


Sure thing, Shashika. Here's the complete Git cheat sheet along with the Contact Details at the end, all bundled up in a single markdown code block:

markdown
Copy code
# 🚀 Git Cheatsheet

> This cheatsheet provides a quick reference guide for the most commonly used Git commands. Happy coding! 👨‍💻

## 📚 Table of Contents

1. [🏁 Initialize Git & Manage Local Changes](#1-initialize-git--manage-local-changes)
2. [🕵️‍♂️ History Inspection & Comparisons](#2-history-inspection--comparisons)
3. [🌴 Branching, Merging & Stashing](#3-branching-merging--stashing)
4. [🤝 Collaboration and Remote Repositories](#4-collaboration-and-remote-repositories)
5. [🔧 Troubleshooting and Miscellaneous Commands](#5-troubleshooting-and-miscellaneous-commands)

---

## 1. 🏁 Initialize Git & Manage Local Changes

> This section covers commands to initialize Git, manage and view local changes.

```git
# Clone Repository
git clone <url> # Clones the repository related to <url>

# Initialize Git
git init # Create a new local repository

# Stage Files
git add <file-name> # Stage a single file
git add . # Stage all the files
git add *.ts # Stage all the files with a pattern

# View the Status
git status # View full status
git status -s # View short status

# Commit Staged Files
git commit -m <message> # Commit with a one-line message
git commit # Open the editor to type a long message

# Commit By Skipping the Staging Area
git commit -am <message> # Stage and commit with a single command

# Remove Files
git rm <file-name> # Remove a file from the working directory and staging area
git rm --cached <file-name> # Remove a file from the staging area only

# View Difference
git diff # Show unstaged changes
git diff --staged # Show staged changes

# View Commit History
git log # View detailed commit history
git log --oneline # View one-line commit history
git log --reverse # View reversed commit history
git log --graph --oneline # View one-line commit history as a graph

# View Single Commit
git show <commit-id> # Show a specific commit
git show HEAD # Show the last commit
git show HEAD~2 # Show two steps before the last commit
git show HEAD~2:<file-name> # Shows <file-name> related to 3rd latest commit

# Unstage Files
git restore --staged . # Unstage all the changes
git restore --staged customer.ts # Unstage customer.ts

# Discard Local Changes
git restore <file-name> # Copy file from staging to the working directory
git restore . # Copy all files from staging to the working directory
git clean -fd # Remove all untracked files (files in the working directory)

# Restore Files To An Earlier Version
git restore --source=HEAD~2 <file-name> # Restore the file to 2 commits earlier
More sections would follow for History Inspection & Comparisons, Branching, Merging & Stashing, Collaboration and Remote Repositories, and Troubleshooting and Miscellaneous Commands.


📬 Contact Details

> If there are any issues when running the application, please contact me.

📧 Email: shashikasvka@gmail.com
📞 Whatsapp: +94 713980787