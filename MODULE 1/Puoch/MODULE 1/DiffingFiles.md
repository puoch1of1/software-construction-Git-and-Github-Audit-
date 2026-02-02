Lecture Summary - Diffing Files

When comparing different versions of code, manually opening files side by side is slow and error-prone. Humans easily miss small but important changes. To solve this, tools like **diff** automatically compare files or directories and show exactly what has changed. Instead of scanning entire files, diff highlights only the modified lines, making it faster and more reliable to understand differences between versions.

For example, below are two versions of the same Python function. At a glance, the difference is subtle.

```python
# rearrange1.py
#!/usr/bin/env python3
import re

def rearrange_name(name):
    result = re.search(r"^([\w .]*), ([\w .]*)$", name)
    if result == None:
        return name
    return "{} {}".format(result[2], result[1])
```

```python
# rearrange2.py
#!/usr/bin/env python3
import re

def rearrange_name(name):
    result = re.search(r"^([\w .-]*), ([\w .-]*)$", name)
    if result == None:
        return name
    return "{} {}".format(result[2], result[1])
```

Using `diff`, Git shows only the changed line:

```bash
diff rearrange1.py rearrange2.py
```

```diff
6c6
<     result = re.search(r"^([\w .]*), ([\w .]*)$", name)
---
>     result = re.search(r"^([\w .-]*), ([\w .-]*)$", name)
```

Here, `<` shows what was removed from the first file, and `>` shows what was added to the second file.

For more complex changes, diff can split modifications into sections, showing changed lines (`c`) and added lines (`a`). This can sometimes feel confusing, so the **unified diff format** is often preferred because it provides surrounding context.

```bash
diff -u validations1.py validations2.py
```

```diff
--- validations1.py
+++ validations2.py
@@ -2,7 +2,8 @@
-    assert type(username) == str, "username must be a string"
+    if type(username) != str:
+        raise TypeError("username must be a string")

@@ -10,5 +11,8 @@
     if not username.isalnum():
         return False
+    # Usernames can't begin with a number
+    if username[0].isnumeric():
+        return False
```

In this format, lines starting with `-` were removed, lines starting with `+` were added, and unchanged lines provide context. This makes it much easier to understand *why* a change was made, not just *what* changed.

Beyond diff, there are other comparison tools like **wdiff**, which compares word by word, and graphical tools such as **meld**, **KDiff3**, and **vimdiff**, which visually highlight differences side by side. These tools help developers clearly understand changes and form the foundation for version control systems like Git, which build on these ideas to manage history and collaboration effectively.

