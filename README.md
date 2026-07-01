# git
simple git version control through CLI (terminal).

\* requires https://git-scm.com/install

\* requires GitHub

## 1: Setup
Implement a project connected to GitHub.

`git config --global user.name <name>` - set username for commits.

`git config --global user.email <email>` - set email (or GitHub private noreply email) for commit at ".patch".

`git init` - initialize a local Git repository in a directory/folder.

`git clone <url>` - download a existing repository instead of `git init`.

## 2: Setup for `git init`
Setting up a newly created GitHub repository

`git branch -M main` - rename current branch (master) to main, which is the default for GitHub.

`git remote add origin <url>` - link the local repository to a repository.

## 3: Staging/committing
Reviewing and pushing changes to GitHub.

`git pull` - pull changes from GitHub repository

`git status` - list all files modified

`git diff` - shows exact line-by-line modifications

`git add <file>` - stages modified file (all files if `git add .` or subdirectory if `git add /path/`) for commit

`git diff --staged` - shows difference between staged files and last commit

`git reset <file>` - unstages file/s

`git commit -m "<message>" -m "<description>"` - puts staged file/s in local version history (description optional)

`git push` - pushes changes to GitHub repository

## 4: Isolating Work
Creating alternate version histories.

`git branch` - list all local branches

`git branch <branch-name>` - creates a new branch without switching to it

`git checkout <branch-name>` - switches to the new branch

`git merge <branch-name>` - combines the specified branch with the <b>active<b> branch

`git branch -d <branch-name>` - deletes a specified branch

