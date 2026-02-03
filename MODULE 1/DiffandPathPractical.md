In this example, a broken Python script (disk_usage.py) is used to demonstrate how diff and patch work in practice. Before fixing the bugs, two copies of the script are created: one kept unchanged for comparison and another used for making fixes. Running the script first helps identify errors instead of guessing what’s wrong.

The first issue is a syntax error caused by a return statement placed outside a function, which is invalid in Python. This is fixed by replacing the return with sys.exit, allowing the script to exit properly with a status code. After fixing that, the script still behaves incorrectly by reporting low disk space even when sufficient space is available.

A closer look at the code reveals a logic error: disk space is being converted to gigabytes twice—once when calling the function and again inside the function itself. Removing one of these conversions fixes the logic bug and allows the script to work as intended.

Once the script is fixed, a diff file is generated to capture only the changes made. This diff file can then be shared with a colleague, who can apply the fixes to their own copy of the script using the patch command. After applying the patch, the script runs successfully.

This example shows how diff and patch can be used to identify changes, package fixes, and apply them elsewhere. However, it also highlights how manual this process is, setting the stage for why version control systems like Git are more powerful and efficient for managing changes and collaboration.