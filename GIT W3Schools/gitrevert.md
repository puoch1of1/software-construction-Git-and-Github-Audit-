# 📌 Git Revert Notes

## 🔹 What Does `git revert` Do?
`git revert` undoes a previous commit by creating a **new commit that reverses the changes**.

✅ It keeps the commit history intact, making it the **safest way to undo changes in shared repositories**.

---

## 🔹 Common Git Revert Commands

```bash
git revert HEAD          # Revert the latest commit
git revert <commit>       # Revert a specific commit by hash
git revert HEAD~2          # Revert a commit further back in history
git revert --no-edit       # Skip commit message editor
git log --oneline           # Show commit history in short form
````

---

## 🔹 Finding the Commit to Revert

Before reverting, find the commit hash using:

```bash
git log --oneline
```

### Example Output

```bash
52418f7 (HEAD -> master) Just a regular update...
9a9add8 Added .gitignore
81912ba Corrected spelling error
3fdaa5b Merge pull request #1
```

👉 Copy the commit hash you want to undo.

---

## 🔹 Running Git Revert

To revert the latest commit:

```bash
git revert HEAD --no-edit
```

### Example Output

```bash
[master e56ba1f] Revert "Just a regular update..."
1 file changed
```

👉 This creates a **new commit that undoes the previous one**.

---

## 🔹 Review Changes After Revert

Check commit history:

```bash
git log --oneline
```

### Example

```bash
e56ba1f Revert "Just a regular update..."
52418f7 Just a regular update...
9a9add8 Added .gitignore
```

---

## ✅ Tips & Best Practices

* Use **`git revert` instead of `git reset`** in shared repositories.
* Always check commit history using `git log --oneline`.
* Use `--no-edit` to skip editing the commit message.

---

## ⚠️ Troubleshooting Git Revert

### ❌ Error: could not revert...

Abort the revert:

```bash
git revert --abort
```

### ❌ Error: could not apply...

Continue the revert:

```bash
git revert --continue
```

---

## 🧠 Quick Summary

* `git revert` does **not delete history**.
* It **adds a new commit that reverses changes**.
* Best for teamwork and production environments.

```
```
