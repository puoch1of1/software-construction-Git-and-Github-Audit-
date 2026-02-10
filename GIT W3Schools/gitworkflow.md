### Git Workflow — Summary & Explanation

The **Git workflow** describes how changes move from your local machine to a shared repository in a controlled, trackable way. Git is distributed, meaning you work locally first, then share when ready.

---

### The Three Core Areas of Git

**Working Directory**
This is where you edit files. Changes here are not tracked yet and can be new, modified, or deleted.

**Staging Area (Index)**
This is a holding area where you decide *what exactly* will go into the next commit. Staging is intentional—it prevents accidental commits.

**Repository**
This is where committed history lives. Once changes are committed, they become part of the project’s timeline.

Flow:

```
Working Directory → Staging Area → Repository
```

---

### Core Workflow Commands

**`git add`**
Moves changes from the working directory into the staging area.

**`git commit`**
Saves staged changes as a permanent snapshot in the local repository.

**`git push`**
Sends local commits to a remote repository so others can access them.

**`git status`**
Shows the current state of files—staged, unstaged, or untracked.

---

### Fixing Mistakes (Before Pushing)

Git lets you correct errors safely if you catch them early.

* Restore changes in files before staging
* Unstage files without losing work
* Edit or update the most recent commit
* Undo a commit while keeping your changes

This safety net is one of Git’s biggest strengths.

---

### Best Practices

Commit often with clear messages that explain *why* a change exists.
Stage only what you intend to commit.
Check status frequently to stay oriented.
Review changes before committing.
Push regularly to share work and avoid large, risky commits.

