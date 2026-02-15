
This section explains how to connect your local machine to GitHub using SSH. After generating your SSH key pair and adding the private key to your SSH agent, you must upload your **public key** to your GitHub account. Without that step, GitHub has no idea who you are when you try to push or pull.

First, copy your public key from your `.ssh` folder. The command differs slightly depending on whether you’re using Windows (Git Bash), macOS, or Linux.

Then:

* Go to GitHub → Profile → Settings
* Open **SSH and GPG keys**
* Click **New SSH key**
* Paste your public key
* Confirm with your password or 2FA

Once added, GitHub links that key to your account. After this, you can use SSH URLs (like `git@github.com:username/repo.git`) to push, pull, and clone securely without entering your password every time.

The deeper idea here is identity through cryptography. Instead of typing a password repeatedly, you prove mathematically that you own a private key that matches the public key GitHub has on file. It’s cleaner, safer, and far more professional than relying on passwords alone.

