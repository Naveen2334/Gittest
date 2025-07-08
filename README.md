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

Bilkul, **`git stash`** ka **“poora panta”** (i.e., full concept + real dev use + commands + interview notes) yahan ekdam clear kar dete hain — bilkul step-by-step, Hindi + code example ke saath.

---

## 🔰 **1. Git Stash Kya Hai?**

> `git stash` ek **temporary locker** hai jo aapke **working directory** ke changes ko **temporarily hata** deta hai bina unhe commit kiye.

* ⚡ Use jab karte hain jab:
  ✅ Aapne kuch changes kiye hain
  ✅ Aapko branch switch karni hai
  ✅ Par aap abhi commit nahi karna chahte

---

## 🧠 **2. Git Stash Kis-Kis Ko Stash Karta Hai?**

| Type                                              | Stash karega?       |
| ------------------------------------------------- | ------------------- |
| ✅ Modified files                                  | ✔️ Yes              |
| ✅ Staged files (`git add` wale)                   | ✔️ Yes              |
| ❌ Untracked files (`git status` mein "Untracked") | ❌ By default **No** |
| ❌ Ignored files (.gitignore)                      | ❌ No                |

> ✅ Tip: Untracked files ko bhi stash karna hai to use:

```bash
git stash -u      # includes untracked files
git stash -a      # includes untracked + ignored files
```

---

## ⚙️ **3. Common Commands + Examples**

### 🔹 `git stash`

Basic stash command – modified + staged changes chhupa deta hai

```bash
git stash
```

---

### 🔹 `git stash list`

Dekho kitne stash bane hain

```bash
git stash list

# Output:
stash@{0}: WIP on main: e2a1bc5 fixed typo
stash@{1}: WIP on dev: added login logic
```

---

### 🔹 `git stash pop`

Last wala stash **nikal ke wapas apply** karta hai aur list se hata deta hai

```bash
git stash pop
```

---

### 🔹 `git stash apply`

Stash wapas apply karega, **lekin stash list mein rahega**

```bash
git stash apply stash@{0}
```

---

### 🔹 `git stash drop`

Specific stash ko delete karne ke liye

```bash
git stash drop stash@{0}
```

---

### 🔹 `git stash clear`

Saare stash hata do

```bash
git stash clear
```

---

## 🧑‍💻 **4. Real-World Developer Use Case**

### 🔁 Situation:

> Aap `main` branch pe ho aur kuch code likh rahe ho, par urgent bugfix ke liye `dev` branch pe jana hai.

```bash
# Aapne changes likhe (but commit nahi kiya)
nano HomeController.java

# Staging bhi kar diya
git add .

# Now: urgent branch switch
git stash         ✅ (code safe ho gaya)
git checkout dev  ✅ (switch hogaya)

# Bug fix karo → commit karo
# Return back
git checkout main

# Code wapas lao
git stash pop     ✅ (code wapas mil gaya)
```

---

## 🛠 Bonus: Interview Notes

| Question                                                    | Interview-Ready Answer                                                                                                       |
| ----------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| ❓ Git stash kya karta hai?                                  | Ye command aapke current changes ko temporarily save karta hai bina commit kiye, taaki aap kisi aur task pe switch kar sako. |
| ❓ Stash aur commit ka difference?                           | Commit permanent hota hai repo mein; stash temporary hota hai jo later apply/drop kiya ja sakta hai.                         |
| ❓ Staged + unstaged changes stash hote hain kya?            | Haan, `git stash` dono ko save karta hai.                                                                                    |
| ❓ Untracked files ka kya?                                   | By default stash nahi hote, use `-u` lagana padta hai.                                                                       |
| ❓ Difference between `git stash pop` and `git stash apply`? | `pop` apply bhi karta hai aur list se hata deta hai, `apply` sirf apply karta hai, stash list mein rehta hai.                |

---

## 📦 Summary Cheatsheet

| Command           | Use                                     |
| ----------------- | --------------------------------------- |
| `git stash`       | Save modified + staged changes          |
| `git stash -u`    | Save untracked files too                |
| `git stash list`  | Show stash stack                        |
| `git stash pop`   | Re-apply last stash + remove from stack |
| `git stash apply` | Re-apply stash (keep it in list)        |
| `git stash drop`  | Remove a specific stash                 |
| `git stash clear` | Remove all stashes                      |

---

Agar chaho toh iska **PDF ya graphic poster** bhi bana ke de sakta ho – ya practice ke liye quiz/daily challenge bhi. Batau?

