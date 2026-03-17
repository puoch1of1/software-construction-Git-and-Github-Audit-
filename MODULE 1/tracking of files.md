:::writing{variant=“standard” id=“63927”}

# Git File Tracking — Lecture Summary

## Introduction

In Git, files are either **tracked** or **untracked**.

- **Tracked files** are files that Git already knows about and monitors for changes.
- **Untracked files** are new files that exist in the project directory but have not yet been added to Git’s tracking system.

When a new file is created, Git initially treats it as **untracked**. Once it is added to Git, it begins moving through a series of states that represent the lifecycle of a change.

---

## File States in Git

Tracked files typically move through three main states:

Modified → Staged → Committed

These stages represent how Git manages changes before permanently recording them in the repository.

---

## Modified State

When a tracked file is edited, Git detects that its contents have changed. At this point, the file enters the **modified** state.

This means:

- The file has been changed in the working directory.
- Git recognizes the modification.
- The changes have **not yet been prepared for saving** in the repository.

You can check the current state of files using:

```bash
git status

If no changes have been made, Git reports that everything is clean:

On branch master
nothing to commit, working tree clean


⸻

Example: Editing a File

Suppose you edit a file using a text editor:

atom disk_usage.py

After saving the changes, Git will recognize that the file has been modified.

Running the status command again:

git status

Git will display something similar to:

modified: disk_usage.py

This indicates that the file has been changed but has not yet been prepared for committing.

⸻

Staging Changes

Before saving changes permanently, Git requires them to be placed in the staging area.

The staging area acts as a preparation step where you select which changes will be included in the next commit.

To stage the modified file:

git add disk_usage.py

After this command, Git marks the file as ready to be included in the next snapshot.

⸻

Committing Changes

Once the desired changes are staged, they can be permanently recorded in the repository through a commit.

A commit creates a snapshot of the current staged files and stores it in the Git repository.

Example commit command:

git commit -m "Add periods to the end of sentences."

Git then records the changes and displays a summary:

1 file changed, 2 insertions(+), 2 deletions(-)

This output indicates how many lines were added or removed as part of the commit.

⸻

Verifying the Repository Status

After committing the changes, running the status command again:

git status

Git will show:

nothing to commit, working tree clean

This message confirms that all tracked changes have been successfully committed and the working directory is synchronized with the repository.

⸻

Key Concept

Git manages file changes through a structured process:
	1.	Modified – A file has been changed but not prepared for saving.
	2.	Staged – The change has been marked for inclusion in the next commit.
	3.	Committed – The change has been permanently recorded in the repository history.

Understanding this workflow is fundamental to using Git effectively for tracking and managing project changes.

:::