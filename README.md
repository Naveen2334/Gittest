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

Here's your complete guide with `git log` commands written in the same clean format as your `## Edit Config` block 👇

---

## 🔥 Most Useful `git log` Commands

### ✅ Short Summary (oneline)

```
git log --oneline
```

➡ Har commit ko ek line me dikhaata hai

---

### 📈 Graph View

```
git log --oneline --graph --all --decorate
```

➡ Branches aur merges ka visual tree dikhata hai

---

### 🧑‍💻 Filter by Author

```
git log --author="Naveen"
```

➡ Sirf un commits ko dikhaata hai jo Naveen ne kiye

---

### 🔎 Search by Commit Message

```
git log --grep="bug fix"
```

➡ Sirf wo commits dikhata hai jinke message me "bug fix" likha ho

---

### 📅 Filter by Date

```
git log --since="2025-07-01"
git log --until="2025-07-08"
git log --since="1 week ago"
```

➡ Specific date range me commit dikhata hai

---

### 📂 Show log of a specific file

```
git log naveengitBatch.txt
```

➡ Sirf us file ke commits dikhata hai jisme change hua

---

### 🧾 Show patch (code diff in log)

```
git log -p
```

➡ Har commit ke saath kya code change hua, wo dikhata hai

---

### 🔢 Limit number of commits

```
git log -n 5
```

➡ Sirf last 5 commits dikhata hai

---

### 🎨 Custom Format Output

```
git log --pretty=format:"%h - %an, %ar : %s"
```

➡ Apne format me log print karo
`%h`: short hash, `%an`: author name, `%ar`: relative date, `%s`: message

**Example Output:**

```
8d632f7 - Naveen Kumar, 2 hours ago : first commit
```

---

### 🎯 Bonus Tip: Show Changed Files Only

```
git log --name-only
```

➡ Har commit ke baad sirf file names dikhata hai jo change hui

---

Would you like this as a downloadable **PDF cheat sheet** or want more `git` commands like `git diff`, `git reset`, etc.?

