Git Merge — Summary & Explanation

Merging in Git is the process of combining changes from one branch into another. It’s how separate lines of work—features, fixes, or experiments—are brought back together into a single project history.

In practice, you usually merge a feature or bug-fix branch into main once the work is complete.

Basic Merge Workflow

Switch to the branch that should receive the changes (usually main)
Run git merge <branch-name>
Git combines the histories and updates the files
If conflicts occur, you resolve them and commit
Common Merge Types

Fast-forward merge Happens when the target branch has not changed since the feature branch was created. Git simply moves the branch pointer forward—no merge commit is created.

No-fast-forward merge (--no-ff) Forces Git to create a merge commit even when a fast-forward is possible. This keeps branch history visible and is common in team projects.

Squash merge (--squash) Combines all commits from a branch into a single commit before merging. Useful for keeping history clean.

Key Merge Commands

git merge branch-name        # Merge a branch
git merge --no-ff branch     # Always create a merge commit
git merge --squash branch    # Combine commits into one
git merge --abort            # Cancel a merge in progress
Merge Conflicts (Core Idea)

A merge conflict happens when two branches modify the same part of a file and Git can’t decide which version is correct.

Git marks conflicts directly in the file using special markers. You must:

Open the file
Decide the final correct content
Remove conflict markers
Stage and commit the fix
Conflicts are normal in collaborative work—they’re not errors, they’re decisions.

After a Successful Merge

Once a branch is merged and no longer needed, it should be deleted to keep the repository clean:

git branch -d branch-name
Best Practices for Merging

Commit or stash changes before merging
Merge frequently to reduce conflicts
Read conflicts carefully—never auto-accept blindly
Use descriptive merge commit messages
Delete merged branches