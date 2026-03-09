
# Connecting Your Local Git Repository to GitHub Using SSH

(Prerequisite: You’ve already generated an SSH key pair and added the **public key** to your GitHub account → Settings → SSH and GPG keys)

## Step 1: Test Your SSH Connection
Run this command in your terminal:

```bash
ssh -T git@github.com
Expected successful output:
Hi your-username! You've successfully authenticated, but GitHub does not provide shell access.
→ This means GitHub recognizes your computer using your private SSH key. If it asks for a password → your SSH setup needs fixing (key not loaded, wrong permissions, etc.).
Step 2: Get the SSH URL of Your Repository
	1	Go to your repository on GitHub
	2	Click the green Code button
	3	Select the SSH tab → URL looks like: git@github.com:your-username/your-repository.git
Copy this URL.
Step 3: Connect Your Local Repository
Option A – First time linking this folder to GitHub
git remote add origin git@github.com:your-username/your-repository.git
Option B – Already have a remote (e.g. HTTPS) and want to switch to SSH
git remote set-url origin git@github.com:your-username/your-repository.git
Step 4: Verify the Remote (Recommended)
git remote -v
You should see:
origin  git@github.com:your-username/your-repository.git (fetch)
origin  git@github.com:your-username/your-repository.git (push)
Step 5: You’re Done!
Now use these commands without passwords:
git push origin main
git pull origin main
# or whichever branch you're working on
Quick Summary – Why SSH > HTTPS
Feature
HTTPS
SSH
Authentication
Username + Password / PAT
Cryptographic key pair
Password prompts
Every push/pull (or cached)
None after initial setup
Security for teams
Token can be revoked/leaked
Private key stays on your machine
Best for
One-off clones, CI/CD tokens
Daily development, frictionless workflow
SSH makes Git feel smooth and secure → teams actually use it consistently.
Happy pushing! 