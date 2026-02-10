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

--HM

### **Summary and Notes: Comparing File Differences Using `diff`**

---

## **1. Purpose of Comparing Files**

When working with multiple versions of code or configuration files, it is important to identify what has changed between them. Manually comparing files by viewing them side by side is possible but unreliable and prone to human error. Automated tools provide a faster and more accurate method of identifying differences.

---

## **2. The `diff` Command**

### **Definition**

`diff` is a command-line tool used to compare two files or directories and display the differences between them.

### **Key Function**

* Highlights only the parts of files that are different.
* Helps developers track changes made between file versions.
* Reduces errors that occur during manual comparison.

---

## **3. Understanding Basic `diff` Output**

When `diff` compares two files, it displays:

* The lines that are different between the files.
* Symbols that indicate the type of change.

### **Common Symbols**

* `<` indicates content removed from the first file.
* `>` indicates content added to the second file.

This usually means an old line in the first file was replaced with a new line in the second file.

---

## **4. Types of Changes Detected by `diff`**

### **a. Changed Lines (`c`)**

* Indicates that content in one file was replaced with content in another file.
* Example format:
  `5c5,6`

  * Shows that line 5 in the first file was changed into lines 5 and 6 in the second file.

---

### **b. Added Lines (`a`)**

* Indicates that new lines were added in the second file.
* Example format:
  `11a13,15`

  * Shows that lines 13 to 15 were added to the second file.

---

## **5. Unified Diff Format (`diff -u`)**

The unified format provides a clearer and more detailed comparison by:

* Showing removed lines with a minus sign (`-`).
* Showing added lines with a plus sign (`+`).
* Including surrounding context lines to help understand where changes occurred.

This format is easier to read and helps users better understand how changes fit into the overall code structure.

---

## **6. Other File Comparison Tools**

### **a. `wdiff`**

* Compares files word by word instead of line by line.
* Useful when small word-level changes need to be identified.

---

### **b. Graphical Comparison Tools**

These tools display files side by side and highlight differences using colors, making them easier to understand visually.

Examples include:

* Meld
* KDiff3
* Vimdiff

---

## **7. Importance of File Comparison Tools**

* Improves accuracy when reviewing changes.
* Helps identify updates, errors, or modifications in code.
* Provides better context for understanding changes.
* Supports collaboration and version tracking.

---

## **8. Key Points to Remember**

* Manual comparison of files is inefficient and unreliable.
* The `diff` tool is widely used for comparing files and directories.
* Unified diff format provides better readability and context.
* Additional tools such as `wdiff` and graphical comparison software offer alternative comparison methods.

---
