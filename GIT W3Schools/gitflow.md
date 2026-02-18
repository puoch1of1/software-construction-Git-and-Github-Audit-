## GitHub Flow — Summary

GitHub Flow is a simple branch-based workflow designed for continuous collaboration and fast delivery. Its core principle is that the `main` (or `master`) branch should always be deployable.

Here’s the process in plain terms:

### 1. Create a Branch

Start new work by creating a branch from `main`. This lets you experiment or build features without breaking stable code. Use clear, descriptive names.

### 2. Make Commits

Work in small, meaningful steps. Commit often with clear messages explaining what changed and why. Each commit becomes part of your project’s history and can be reverted if needed.

### 3. Open a Pull Request (PR)

When your work is ready for review, open a pull request. This signals that your changes are ready for feedback or merging.

### 4. Review and Discuss

Team members review the code, suggest improvements, and discuss decisions. You can push more commits to the same branch if changes are requested.

### 5. Deploy and Test

Before merging, deploy the branch to test it in a real or staging environment. If something fails, revert to the stable `main` branch.

### 6. Merge

Once approved and tested, merge the branch into `main`. The pull request remains as a record of what changed and why.

---

### Core Idea

* `main` is always stable and production-ready.
* All new work happens in branches.
* Collaboration happens through pull requests.
* Deployment can happen before merging.

It’s lightweight, beginner-friendly, and scales well for teams practicing continuous integration and continuous delivery.
