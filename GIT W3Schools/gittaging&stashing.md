---

# **Git — Staging & Stashing**

---

## **1. Git Staging (Staging Area)**

**Purpose:**
Temporarily hold changes you want to include in the next commit. Think of it as a selection step between editing files and saving them permanently.

**Why it matters:**

* Choose exactly which changes go into a commit.
* Create clean, focused commits.
* Prevent unfinished or accidental changes from being committed.

**Workflow:**

1. Edit files in the working directory.
2. Stage selected changes: `git add <file>`
3. Commit staged changes: `git commit -m "message"`

**Commands:**

| Action              | Command                                                          |
| ------------------- | ---------------------------------------------------------------- |
| Stage a single file | `git add index.html`                                             |
| Stage all changes   | `git add --all` or `git add -A`                                  |
| Check staged files  | `git status`                                                     |
| Unstage a file      | `git restore --staged index.html` or `git reset HEAD index.html` |

**Key Concept:**

> Staging allows you to select which changes will go into the next commit.

---

## **2. Git Stashing**

**Purpose:**
Temporarily save uncommitted changes to return to a clean working directory. Designed for **interruptions**, not long-term storage.

**Why it matters:**

* Switch branches safely without committing unfinished work.
* Pause work to fix urgent issues.
* Preserve work-in-progress without messy commits.

**What gets stashed:**

* Tracked files ✔
* Untracked files (only if included: `git stash -u`)

**Commands:**

| Action                   | Command                                 |
| ------------------------ | --------------------------------------- |
| Stash changes            | `git stash`                             |
| Stash with message       | `git stash push -m "WIP: feature"`      |
| List stashes             | `git stash list`                        |
| Show stash details       | `git stash show` or `git stash show -p` |
| Apply latest stash       | `git stash apply`                       |
| Apply specific stash     | `git stash apply stash@{n}`             |
| Apply & remove stash     | `git stash pop`                         |
| Delete a specific stash  | `git stash drop stash@{n}`              |
| Delete all stashes       | `git stash clear`                       |
| Create branch from stash | `git stash branch <branchname>`         |

**Stash Stack Concept:**

* Newest stash = `stash@{0}`
* Older stashes move down the stack
* Can apply, drop, or branch from any stash

**Best Practices:**

* Use clear stash messages
* Don’t rely on stashes as backups
* Clean up old stashes regularly
* Expect merge conflicts across branches

---

### **Quick Comparison**

| Feature  | Staging                          | Stashing                                   |
| -------- | -------------------------------- | ------------------------------------------ |
| Purpose  | Select changes for next commit   | Save unfinished changes temporarily        |
| Usage    | Prepares changes for Git history | Handle interruptions without committing    |
| Scope    | Only staged files                | All tracked changes (optionally untracked) |
| Workflow | `edit → stage → commit`          | `edit → stash → switch/fix → apply`        |

---

### **One-Line Summaries**

* **Staging:** Choose which changes go into the next commit.
* **Stashing:** Temporarily save uncommitted changes to switch tasks safely.

---

