
### Git Stashing — Simple Summary

**Git stash** temporarily saves your uncommitted changes so you can return to a clean working directory without committing unfinished work.
It’s designed for **interruptions**, not long-term storage.

Think of it as putting your work in a safe drawer, handling something urgent, then pulling it back out.

---

### Why Git Stash Is Used

* Switch branches safely without committing
* Pause work to fix urgent bugs
* Keep work-in-progress without messy commits
* Avoid losing local changes

---

### What Gets Stashed

* Tracked files (staged and unstaged) ✔
* Untracked files  (unless explicitly included)

To include untracked files:

```
git stash -u
```

---

### Core Git Stash Commands

**Stash your changes**

```
git stash
```

**Stash with a message**

```
git stash push -m "WIP: feature name"
```

**List all stashes**

```
git stash list
```

**View stash contents**

```
git stash show
git stash show -p
```

**Apply the latest stash (keep it)**

```
git stash apply
```

**Apply a specific stash**

```
git stash apply stash@{n}
```

**Apply and remove the stash**

```
git stash pop
```

**Delete a specific stash**

```
git stash drop stash@{n}
```

**Delete all stashes (permanent)**

```
git stash clear
```

**Create a branch from a stash**

```
git stash branch <branchname>
```

---

### The Stash Stack (Key Concept)

Each stash is saved in a **stack**:

* Newest stash is `stash@{0}`
* Older stashes move down the stack
* You can apply, drop, or branch from any stash

---

### Best Practices

* Always use clear stash messages
* Don’t treat stashes as backups—commit when ready
* Clean up old stashes regularly
* Expect merge conflicts when applying stashes across branches

---

**Git stash temporarily saves uncommitted changes so developers can switch tasks without committing unfinished work.**

---

