# Initialize GIT
git init => create a new local repository

# Rename Branch
git branch -m <name> [local] => rename the current branch

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