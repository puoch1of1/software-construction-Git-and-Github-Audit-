Lecture Summary Git Commands

Git is a version control system that helps track file changes, manage project history, and support collaboration. Every Git project is organized into three main parts that work together to track and store changes.

The first part is the **Git directory**. This is the hidden `.git` folder that acts like the brain of the project. It stores the entire history of changes, commits, and metadata. The second part is the **working tree**, which contains the current version of the project files that you actively edit. The third part is the **staging area**, which temporarily stores selected changes before they are permanently saved in the repository. Together, these three sections allow Git to track progress through snapshots of your project.

---

### Configuring Git Identity

Git needs to know who is making changes so it can label commits correctly. This is done using the `git config` command.

```bash
git config --global user.email "me@example.com"
git config --global user.name "My Name"
```

The `--global` flag applies these settings to all repositories on your machine.

---

### Creating a Repository

To start tracking a project, Git must initialize a repository using:

```bash
git init
```

This creates a `.git` directory inside your project folder.

---

### Checking Directory Contents

To confirm that Git created its internal directory, you can list files using:

```bash
ls -la
```

To view the contents of the Git directory itself:

```bash
ls -l .git/
```

This directory stores project history and version tracking data.

---

### Tracking Files with Git

To make Git track a file and prepare it for saving, you use the `git add` command. This places changes into the staging area.

```bash
git add disk_usage.py
```

The staging area acts like a preparation zone where you select which changes will be included in the next snapshot.

---

### Checking Project Status

The `git status` command shows the condition of your project, including modified files, staged files, and pending changes.

```bash
git status
```

This command is useful for understanding what Git is currently tracking.

---

### Saving Changes with Commits

Once changes are staged, they are permanently recorded using the commit command.

```bash
git commit
```

Running this command opens a text editor where you write a commit message explaining the change. The commit moves changes from the staging area into the Git directory as a saved snapshot.

---

### Writing Effective Commit Messages

Commit messages improve communication and make project history easier to understand. A strong commit message contains two main parts:

**Summary**

* First line of the message
* About 50 characters or fewer
* Briefly explains the change

**Description**

* Written below a blank line
* Each line kept under 72 characters
* Explains why the change was made
* Can include references to bugs, tickets, or documentation links

Example structure:

```text
Add disk usage monitoring feature

Introduces a new script that checks available disk space and alerts
users when storage falls below a safe threshold. Fixes issue #42.
```

---

### Key Takeaways

Understanding Git’s structure and commands helps manage projects effectively. Using commands like `git init`, `git add`, `git status`, and `git commit` allows you to track changes and maintain organized version history. Writing clear commit messages strengthens collaboration and makes future debugging or updates far easier.
