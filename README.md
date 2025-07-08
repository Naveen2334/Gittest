# Git Commands Guide

## Check Git Version
```
git --version
```

## Set Config Name and Email
```
git config --global user.name "Naveen Kumar Barnwal"
git config --global user.email "naveenkumar16613@gmail.com"
```

## Check Config Values
```
git config --global user.name
git config --global user.email
```

## Edit Config
```
git config --global --edit
```
After editing in VS Code, open terminal and write:
```
Esc  then write :wq  press Enter
```

## Navigate to File Location
```
cd <File Name>
```

## List Files
```
ls
```

## Initialize Git Repository
```
git init
```

## List All Files (Including Hidden)
```
ls -a
```

## Check Untracked Files
```
git status
```

## Add a Specific File to Staging
```
git add sum.java
```

## Commit Changes
```
git commit -m "initial commit"
```

## View Commit Logs
```
git log
```

## Switch Between Commits or Branches
```
git checkout <Hashcode/branch name>
```

## View All Branches
```
git branch
```

## Create a New Branch
```
git branch dev
```

## Create a Branch with a Specific Name
```
git checkout -b anuj/multiply
```

## Merge Branch into Dev
```
git merge anuj/multiply
```

## Merge Dev into Master
```
git checkout master
git log
git merge dev
```

## Create a .gitignore File
```
touch .gitignore
```

## Check Remote Repository
```
git remote -v
```

## Add Remote Repository
```
git remote add origin https://github.com/Naveen2334/Git.git
```

## Verify Remote Repository
```
git remote -v
```

## Rename Branch to Main
```
git branch -M main
```

## Push to Remote Repository
```
git push -u origin main
```

## Check Status After Modifications
```
git status
```

## Stage Changes
```
git add sum.java
```

## Commit Changes
```
git commit -m "new changes added

```

## Git restore

```

| Situation                             | Command                                     | Result                                          |
| ------------------------------------- | ------------------------------------------- | ----------------------------------------------- |
| Uncommitted changes hataane hain      | `git restore file.txt`                      | File waapas last commit jaisi ho jaayegi        |
| Staged file ko unstage karna          | `git restore --staged file.txt`             | `git add` ka effect hata dega                   |
| Dono hataane hain                     | `git restore --staged --worktree file.txt`  | File clean ho jaayegi                           |
| File kisi purane commit jaisi chahiye | `git restore --source=<commit-id> file.txt` | File us commit ke content se replace ho jaayegi |

```

## Push Changes to Remote
```
git push
```
