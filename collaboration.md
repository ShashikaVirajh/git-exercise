# Git Collaboration

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
