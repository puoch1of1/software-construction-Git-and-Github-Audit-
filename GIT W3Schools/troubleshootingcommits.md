### Troubleshooting Common Commit Mistakes

**Forgot to stage a file?**
If you run git commit -m "message" but forgot to git add a file, just add it and commit again. Or use git commit --amend to add it to your last commit.
**Typo in your commit message?**
Use git commit --amend -m "Corrected message" to fix the last commit message.
**Accidentally committed the wrong files?**
You can use git reset --soft HEAD~1 to undo the last commit and keep your changes staged.