# git
simple git version control

## 1: Setup
Implement a project connected to GitHub

```
# set to your github username for consistency
git config --global user.name "placeholder"

# set your email (or GitHub noreply email)
git config --global user.email "123456789+username@users.noreply@githu.com"
```

## git repo
Create a repository on GitHub

```
# initalize git in a folder through the terminal
git init
```

Stage all files for next commit
```
git add .
```

Create commit
```
git commit -m "feat: Changed something"
```

Change the current branch name to "main" rather than master
```
git branch -M main
```

Connect current working directory to Git
```
git remote add origin <repo link>
```

Push commit to main branch
```
git push -u origin main
```
