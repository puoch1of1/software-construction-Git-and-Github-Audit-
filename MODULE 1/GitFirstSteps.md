
When you start using Git, the first thing it needs to know is **who you are**, because Git records who made each change.

You set this once using configuration:

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

The `--global` flag means this applies to all Git projects on your computer. You can also set different names or emails per project if you want.

---

There are **two ways to start using Git** in a project:

1. Create a brand-new repository
2. Copy an existing one

To create a new repository, you make a folder and run:

```bash
git init
```

This creates a hidden folder called `.git`. You can see it with:

```bash
ls -la
```

The `.git` folder is Git’s **database**. It stores the history of changes. You never edit anything in there directly—Git handles it for you.

---

Everything **outside** the `.git` folder is called the **working tree**.
This is where you actually edit files.

At first, the working tree might be empty. Once you add a file (for example `disk_usage.py`), Git sees it but **does not track it yet**.

---

To tell Git to track a file, you add it to the **staging area**:

```bash
git add disk_usage.py
```

The staging area is a holding place for changes you want to save next.

You can check what’s going on at any time with:

```bash
git status
```

If Git says the file is “ready to be committed,” it’s in the staging area.

---

To permanently save the change, you commit it:

```bash
git commit
```

Git opens a text editor so you can write a **commit message** explaining what you did. For example:

```
Add disk usage script
```

When you save and exit, Git stores that change in the `.git` directory.

---


