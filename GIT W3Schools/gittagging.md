### Git Tagging — Simple Summary

**Git tags** are labels (or bookmarks) that point to a specific commit in your project’s history.
They are mainly used to **mark important moments**, such as releases, milestones, or stable versions.

Unlike branches, tags **do not move**. Once created, a tag always points to the same commit unless you force-update it.

---

### Why Tags Are Useful

* Mark releases like `v1.0`, `v2.0`
* Identify stable or deployable versions
* Easily return to or fix older versions
* Help deployment tools know which version to use

---

### Types of Git Tags

**Lightweight tags**

* Just a name pointing to a commit
* No extra information

```bash
git tag v1.0
```

**Annotated tags (recommended)**

* Store author, date, and a message
* Best for releases and shared projects

```bash
git tag -a v1.0 -m "Version 1.0 release"
```

---

### Tag a Specific Commit

You can tag an older commit using its hash:

```bash
git tag v1.1 1a2b3c4d
```

---

### View Tags

**List all tags**

```bash
git tag
```

**See details about a tag**

```bash
git show v1.0
```

---

### Pushing Tags to GitHub (Very Important)

Tags are **local by default** and are NOT pushed with normal commits.

**Push one tag**

```bash
git push origin v1.0
```

**Push all tags**

```bash
git push --tags
```

---

### Deleting Tags

**Delete a local tag**

```bash
git tag -d v1.0
```

**Delete a remote tag**

```bash
git push origin --delete tag v1.0
```

---

### Updating or Replacing a Tag (Use Carefully)

```bash
git tag -f v1.0 <new-commit-hash>
git push --force origin v1.0
```

This rewrites history for anyone using that tag, so only do this when necessary.

---

### Best Practices

* Use **annotated tags** for releases
* Create tags only after tests pass
* Push tags explicitly to the remote
* Avoid force-updating shared tags unless absolutely necessary

---

**Git tagging is used to label specific commits, usually to mark releases, milestones, or stable versions.**

---

Git tags turn your commit history into a **clearly labeled timeline**, making collaboration, deployment, and maintenance far easier.
