Here’s the clean, no-nonsense version, with the important ideas and the code encoded where it helps.

---

A **commit message** is not decoration. It’s documentation for humans—especially future you and teammates who weren’t in your head when you made the change. A good message explains **what changed and why**, not just that something changed.

When writing a commit message, think about someone reading it months later. What context would they need? Was the change tricky? Did it fix a bug or relate to a ticket? Extra clarity now saves serious confusion later.

---

### What a good commit message looks like

A proper commit message has a clear structure:

• **First line**: short summary (about 50 characters)
• **Blank line**
• **Body**: detailed explanation, lines kept under ~72 characters

Example commit message content:

```text
Provide a good commit message example

The purpose of this commit is to provide an example of a well-written
commit message. The first line is a short summary, followed by a blank
line. The paragraphs below explain why the change was made and what it
does, with each line kept under 72 characters.

Additional paragraphs can be added if more explanation is needed,
including links to issues, tickets, or bugs.
```

Lines starting with `#` are comments added by Git. They are **not saved** and only act as reminders:

```text
# Please enter the commit message for your changes.
# Lines starting with '#' will be ignored.
# Changes to be committed:
#   new file: super_script.py
#   new file: cool_config.txt
```

---

### What *not* to do

Avoid vague messages like:

```text
update
fix
change
```

These are useless when browsing history. They explain nothing and slow everyone down later.

---

### Viewing commit history

Git stores commit messages and metadata, which you can view with:

```bash
git log
```

Example output:

```text
commit d8e139cc4f7dcd13b75cff67cfb68527e24c59c5 (HEAD -> master)
Author: My name <me@example.com>
Date:   Thu Jul 11 17:19:32 2019 +0200

    Add a check_reboot function

commit 6cfc29966acda8213fcd8ac2735b31f3fdbc6c53
Author: My name <me@example.com>
Date:   Thu Jul 11 12:08:46 2019 +0200

    Create and empty all_checks.py
```

Each entry shows:
• a unique commit ID
• the author’s name and email
• the date and time
• the commit message

This is why clarity matters—**git log is how your work is remembered**.

---

