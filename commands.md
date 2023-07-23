# Initialize GIT
git init => create a new local repository

# Rename Branch
git branch -m <new-name> => rename the current branch
git branch -m <old-name> <new-name> => rename a different branch

# Push New Branch To Origin
git push origin :<old-branch-name> <new-branch-name> -u => delete old branch on origin and push the new branch. Upstream.

# Stage Files
git add <file-name> => stages a single file
git add . => stages multiple files
git add *.ts => stages with a pattern

# View The Status
git status => full status
git status -s => short status

# Commit Staged Files
git commit -m <message> => commits with a one-line message
git commit => opens the editor to type a long message

# Commit By Skipping Staging Area
git commit -am <message> => staging and committing with a single command

# Remove Files
git rm <file-name> => removes from working directory and staging area
git rm --cached <file-name> => removes from stating area only
[after both theset commands, changes should be commited]

# View Difference
git diff => shows unstaged changes
git diff --staged => shows staged changes

# View Commit History
git log => detailed commit history
git log --oneline => one line commit history
git log --reverse => reversed commit history

# View Single Commit
git show <commit-id> => shows the specific commit
git show HEAD => shows the last commit
git show HEAD~2 => shows two steps before the last commit
git show HEAD:customer.ts => shows the version of customer.ts of the last commit

# Unstage Files
git restore --staged . => unstage all the changes
git restore --staged customer.ts => unstage customer.ts

# Discard Local Changes
git restore <file-name> => copy file from staging to working directory
git restore . => copy all files from staging to working directory
git clean -fd => remove all untracked files (files in working directory)

# Restore Files To An Earlier Version
git restore --source=HEAD~2 <file-name> => restore the file to 3 commits earlier