Lecture Summary - Tracking Files
---

Files in Git can be **tracked** or **untracked**.

New files start as untracked. Once Git tracks a file, it moves through three states:

Modified → Staged → Committed

---

When you edit a file, it becomes **modified**. Git notices the change but hasn’t saved it yet.

You can see this with:

```bash
git status
```

If nothing has changed, Git says the working tree is clean:

```bash
On branch master
nothing to commit, working tree clean
```

---

Now you edit a file, for example:

```bash
atom disk_usage.py
```

After editing, Git shows the file as modified:

```bash
git status
```

```text
modified: disk_usage.py
```

This means the file is changed, but **not ready to be saved**.

---

To mark the change for saving, you add it to the **staging area**:

```bash
git add disk_usage.py
```

Now Git knows this change should be part of the next snapshot.

---

To permanently store the change, you commit it:

```bash
git commit -m "Add periods to the end of sentences."
```

Git creates a new snapshot and stores it in the Git directory. It even shows you what changed:

```text
1 file changed, 2 insertions(+), 2 deletions(-)
```

---

If you check the status again:

```bash
git status
```

You’ll see:

```text
nothing to commit, working tree clean
```
---