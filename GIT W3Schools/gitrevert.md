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
