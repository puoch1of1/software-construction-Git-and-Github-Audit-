**Applying Changes** refers to the process of sharing and updating code efficiently by focusing only on what has been modified rather than replacing entire files. Developers use tools like `diff` to compare two versions of a file and generate a patch (or diff) file that highlights the exact changes along with useful context. These changes can then be automatically applied to the original code using the `patch` command, reducing manual editing and minimizing errors. This approach improves collaboration, maintains clear version history, and is especially useful in large projects where multiple files and directories may be updated, ensuring that modifications are structured, traceable, and easier to integrate.
Notes: Using diff and patch for Code Fixes

1. Purpose of diff and patch

diff and patch are tools used to identify, share, and apply changes made
to code files. They help developers collaborate efficiently without
sending entire files and make debugging and version tracking easier.

2. What is a Diff File?

A diff file shows the differences between an old version of a file and a
new version of a file. It is sometimes called a patch file. It contains
lines that were removed, lines that were added, and extra context around
the changes.

3. Creating a Diff File

Command: diff -u old_file new_file > change.diff

Explanation: - diff compares two files. - -u adds extra context to help
understand changes. - > redirects the output into a file. - change.diff
stores the differences.

4. What is the Patch Command?

The patch command applies changes automatically from a diff file and
removes the need to manually edit code.

Command: patch file_to_modify < change.diff

Explanation: - patch applies the modifications. - < sends diff file
contents as input. - The original file is updated with the changes.

5. Example Scenario

Problem: A CPU monitoring script always reported normal usage even when
CPU load was high.

Cause: The cpu_percent() function was called without a parameter.
Without the parameter, the function always returned zero.

Fix Made: - Added parameter 1 to measure CPU usage over time. - Added a
debugging line to print CPU usage.

Solution: The fix was shared as a diff file and applied using the patch
command.

6. Advantages of Using diff and patch

Efficiency: Only shares changes instead of full files.

Version Flexibility: Works even if the receiver has a slightly different
file version.

Better Collaboration: Clearly shows what was modified.

Useful for Large Projects: Can compare entire directories and manage
updates across multiple files.

7. Key Symbols to Remember

  Redirects output to a file < Sends file contents as input

8. Key Takeaway

diff finds and records changes between files. patch applies those
recorded changes automatically.
