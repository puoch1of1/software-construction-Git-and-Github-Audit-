# Git Revert — Explanation and Summary

## What `git revert` Does

`git revert` is used to **undo the effects of a previous commit by creating a new commit that reverses those changes**.

Unlike other undo methods, it **does not remove commits from the project history**. Instead, it adds a new commit that cancels the changes introduced by an earlier commit.

Because the commit history remains intact, `git revert` is considered the **safest method for undoing changes in shared repositories** where multiple developers are collaborating.

---

## Common Git Revert Commands

Revert the most recent commit:

```bash
git revert HEAD

Revert a specific commit using its hash:

git revert <commit-hash>

Revert a commit further back in history:

git revert HEAD~2

Revert without opening the commit message editor:

git revert --no-edit

View a shortened commit history:

git log --oneline


⸻

Finding the Commit to Revert

Before running git revert, you must identify the commit that introduced the change you want to undo.

You can find the commit hash using:

git log --oneline

Example output:

52418f7 (HEAD -> master) Just a regular update...
9a9add8 Added .gitignore
81912ba Corrected spelling error
3fdaa5b Merge pull request #1

Each commit has a unique hash identifier. Copy the hash of the commit you want to revert.

⸻

Running Git Revert

To undo the most recent commit:

git revert HEAD --no-edit

Example output:

[master e56ba1f] Revert "Just a regular update..."
1 file changed

This command creates a new commit that reverses the changes introduced by the previous commit.

⸻

Reviewing Changes After Revert

After performing the revert, you can confirm the change by checking the commit history:

git log --oneline

Example:

e56ba1f Revert "Just a regular update..."
52418f7 Just a regular update...
9a9add8 Added .gitignore

The new revert commit appears at the top of the history.

⸻

Tips and Best Practices
	•	Use git revert instead of git reset when working in shared repositories.
	•	Always review commit history using git log --oneline before reverting.
	•	Use --no-edit when you want to skip editing the automatically generated commit message.
	•	Reverting maintains a clear and traceable project history.

⸻

Troubleshooting Git Revert

Error: could not revert

If a revert process fails or you want to cancel it:

git revert --abort


⸻

Error: could not apply

If Git pauses the revert due to conflicts, resolve the conflicts and then continue:

git revert --continue


⸻

Key Concept

The most important idea behind git revert is that it preserves the project’s history.

Instead of deleting or rewriting commits:
	•	The original commit remains in the history
	•	A new commit is created to reverse its changes

This approach ensures transparency and safety, especially in collaborative environments.

⸻

Quick Summary
	•	git revert does not delete commits
	•	It creates a new commit that reverses previous changes
	•	It is the recommended method for undoing changes in shared repositories
	•	It maintains a complete and reliable project history

