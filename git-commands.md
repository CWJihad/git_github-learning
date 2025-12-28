# Git Commands Notes

> These commands are for Git Bash / Linux (not the same as PowerShell)

## Initialize repository

```bash
git init
# initialize git in the current project
```

## Add files

```bash
git add file_name
# move file to staging area
```

```bash
git add .
# add all files to staging
```

## Commit changes

```bash
git commit -m "message"
# save staged changes
```

```bash
git commit -am "message"
# add + commit tracked files in one step
# new files still require: git add file_name
```

## Check status

```bash
git status
# show current state of working directory and staging
```

## View commit history

```bash
git log
# full history
```

```bash
git log --oneline
# short history view
```

## Configure user

```bash
git config --global user.name "Your Name"
# set username
```

```bash
git config --global user.email "your@email.com"
# set email
```

```bash
git config --list
# see all git configuration values
```

## Rename or move tracked files

```bash
git mv old_name new_name
# safely rename or move a tracked file/folder
```

## Exit log view

```bash
q
# quit log screen
```

## Remove files and folders

```bash
git rm file_name
# delete tracked file
```

```bash
git rm -r folder_name
# delete folder and contents
```

```bash
git rm --cached file_name
# stop tracking file but keep it locally
```

```bash
git rm --cached folder_name
# stop tracking folder (add to .gitignore after this)
```

## Branches

```bash
git branch
# list branches
```

```bash
git branch branch_name
# create branch
```

```bash
git branch -M new_branch_name
# rename current branch
```

```bash
git branch -d branch_name
# delete branch
```

## Switch branches

```bash
git switch branch_name
# switch to branch
```

```bash
git checkout branch_name
# alternative switch command
```

```bash
git switch -c branch_name
# create and switch to branch
```

```bash
git checkout -b branch_name
# same: create + switch
```

## Merge branches

```bash
git merge branch_name
# merge branch into current branch
# example: checkout main first, then merge into main
```

## Show differences

```bash
git diff --staged
# compare staged changes to last commit
```

```bash
git diff commit1..commit2
# compare two commits
```

## Stash changes

```bash
git stash
# save uncommitted work temporarily
```

```bash
git stash pop
# restore and remove stash
```

```bash
git stash list
# view all stashes
```

```bash
git stash apply stash@{n}
# apply specific stash without deleting it
```

## Checkout commits

```bash
git checkout <commit-id>
# move to previous commit state
```

```bash
git checkout HEAD~2
# go back two commits from current head
```

## Rebase

```bash
git rebase master
# rewrite history into a single straight line
# avoid using on main/master directly
```

## Remote repositories

```bash
git remote -v
# show connected remotes
```

```bash
git remote add origin url
# connect local repo to GitHub
```

```bash
git remote rename old new
# rename remote
```

```bash
git remote remove name
# remove remote
```

## Push to GitHub

```bash
git push -u origin main
# first push and set upstream
```

```bash
git push
# push next commits
```

## Clone repository

```bash
git clone <url>
# download repository
```

## Fetch and pull

```bash
git fetch
# get updates without merging
```

```bash
git pull
# fetch + merge into current branch
```