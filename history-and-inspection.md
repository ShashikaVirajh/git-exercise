# Git History and Inspection

## View The History

- `git log --stat`: Shows the list of modified files.
- `git log --patch`: Show the modified files with changes.

## Filter History

- `git log -<number>`: Shows the last `<number>` commits. 
- `git log --author="<author-name>"`: Shows commits of `<author-name>`.
- `git log <file-name>`: Commits that are related to `<file-name>`.

## View a Commit 

- `git show HEAD~2`: Shows a 3rd latest commit.
- `git show HEAD~2:<file-name>`: Shows `<file-name>` related to 3rd latest commit.

## Compare Commits

- `git diff HEAD~2 HEAD`: Shows the changes between two commits.
- `git diff HEAD~2 HEAD <file-name>`: Shows the changes between two commits related to `<file-name>`.

## Display Contributors

- `git shortlog`: Shows contributors.
- `git shortlog -n`: Shows contributors and commits.
- `git shortlog -s`: Shows contributors with the number of commits.

## Display Author of Lines

- `git blame <file-name>`: Shows the author of each line in `<file-name>`.
