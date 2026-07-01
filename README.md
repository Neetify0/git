# git
simple git version control through CLI (terminal).

\* requires https://git-scm.com/install

\* requires GitHub (other Git hosting software can be used but this documentation was created for GitHub)

## 1: Setup
Implement a project connected to GitHub.

`git config --global user.name <name>` - set username for commits.

`git config --global user.email <email>` - set email (or GitHub private noreply email) for commit.

`git init` - initialize a local Git repository in a directory/folder.

`git clone <url>` - download an existing repository instead of `git init`.

## 2: Setup for `git init`
Setting up an initialized local GitHub repository

`git branch -M main` - rename current branch (master) to main, which is the default for GitHub.

`git remote add origin <url>` - link the local repository to a remote repository.

## 3: Staging/committing
Reviewing and pushing changes to GitHub.

`git fetch` - downloads data but does not merge.

`git pull` - fetches and merges data.

`git status` - list all files modified (untracked, modified, and staged).

`git diff` - show exact line-by-line modifications.

`git add <file>` - stage modified file (all files if `git add .` or subdirectory if `git add ./path/`/`git add path/`) for commit.

`git diff --staged` - show the difference between staged files and last commit.

`git reset <file>` - unstage file/s.

`git reset --soft HEAD~1` - undo last commit and keep its changes staged

`git reset --hard HEAD~1` - delete last commit and its changes from **LOCAL** version history

`git commit -m "<message>" -m "<description>"` - put staged file(s) in local version history (description optional).

`git commit --amend -m "<message>" -m "<description>"` - modify most recent commit (**NEVER** amend pushed commits) 

`git push -u origin <branch-name>` (main is usually the default) - push changes to GitHub repository for the very first time (see section 4 for information on branching).

`git push` - push changes to GitHub repository.

## 4: Isolating work
Creating alternate version histories.

`git branch` - list all local branches.

`git branch <branch-name>` - create a new branch without switching to it.

`git checkout <branch-name>` - switch to the new branch.

`git merge <branch-name>` - merge changes from the specified branch into your **ACTIVE** branch.

`git branch --delete <branch-name>` - delete a specified branch.

`git push origin --delete <branch-name>` - delete branch on remote repository

## 5: Stash changes
`git stash` - put away changes temporarily so you can freely switch branches without committing work.

`git stash list` - list stashed sets.

`git stash pop` - return stashed changes.

## 6: Version history
`git log` - check commit history with an associated id (SHA).

`git checkout <commit-SHA>` - move working directory safely to a commit.

`git checkout main` (or current branch) - bring workspace back to present.

`git revert <commit-SHA>` - create commit which undoes the specific changes of that specific commit, without wiping any work after it.

## 7: Information and resources
More information can be found at the [documentation](https://git-scm.com/cheat-sheet) or online.

Additional resources:
- https://www.youtube.com/watch?v=HkdAHXoRtos
- https://www.youtube.com/watch?v=MJUJ4wbFm_A
