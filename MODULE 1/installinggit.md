# Installing Git on Windows – Lecture Summary

## Overview
This guide covers installing **Git for Windows** from the official site (gitforwindows.org).  
The installer bundle includes:
- Git command-line tools
- Bash emulation environment (Git Bash)
- Unix-like utilities
- Git GUI (optional – not covered in detail in the course)

## Step-by-Step Installation

1. **Download**  
   - Go to **https://gitforwindows.org**  
   - Download the latest version

2. **Run the Installer**  
   - Click **Keep** when the browser security prompt appears

3. **License Agreement**  
   - Git is released under **GPL v2** (free software – source code visible & modifiable)  
   - Accept and continue

4. **Installation Path**  
   - Keep the default path (recommended)

5. **Selecting Components** (recommended defaults)  
   - Windows Explorer integration (right-click → Git options in folders)  
   - Git LFS (Large File Storage) support – keep enabled  
   - Associate .gitconfig / .gitattributes with text editor  
   - Associate .sh files to be run with Bash  
   - Optional extras: desktop icons, TrueType fonts in console, auto-check for updates

6. **Start Menu Folder**  
   - Default: “Git” (keep as is)

7. **Choosing the Default Editor**  
   - Most important personal choice  
   - Common options: Notepad++, Visual Studio Code, Sublime Text, Atom, etc.  
   - Can manually enter path to any editor executable  
   - Course example: **Atom** (must be installed separately)

8. **Adjusting the PATH Environment**  
   Recommended choice:  
   - **Git from the command line and also from 3rd-party software** (2nd option, pre-selected)  
     → Git available in Git Bash + Windows Command Prompt  
     → Safe balance – does not override Windows tools  
   Other options:  
   - Only Git Bash (most restricted)  
   - Git + full Unix tools (may override Windows commands – usually not recommended)

9. **HTTPS Transport Backend**  
   - Default: **Use the OpenSSL library** (recommended for GitHub, public repositories)  
   - Alternative: Use Windows native library (better for some corporate proxies / internal systems)

10. **Configuring Line Endings** (CRLF vs LF)  
    Recommended (default):  
    - **Checkout Windows-style, commit Unix-style line endings**  
      → Best for cross-platform collaboration (Windows + Linux/macOS)  
    Other options:  
    - As-is (no conversion) – only if all team members use same OS  
    - Checkout as-is, commit Unix-style – for Unix-like workflow on Windows

11. **Terminal Emulator**  
    Recommended: **Use MinTTY** (default terminal provided by Git for Windows)  
    → Better Unicode support, scrollback history, etc.  
    Alternative: Use Windows' default console

12. **Extra Options**  
    Recommended defaults:  
    - Enable file system caching (performance)  
    - Enable Git Credential Manager  
    - Symbolic links: usually leave disabled (unless needed)

13. **Experimental Features**  
    - Optional and change over time  
    - Recommendation for beginners: leave them **disabled** (safer, more stable)

14. **Install**  
    - Click **Install** and wait for completion

## Final Result
After installation you will have:
- **Git Bash** – full Unix-like shell with Git commands
- Git available in Windows Command Prompt / PowerShell
- Basic Git GUI (optional)
- All tools needed for the rest of the Git course

## Additional Resources
- Check the next reading in the course for more installation help and links

---
**Note**: Always choose editor and line-ending settings based on your workflow and team collaboration needs.