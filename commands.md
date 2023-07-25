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
