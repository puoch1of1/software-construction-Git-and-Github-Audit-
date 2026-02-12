
This page explains how to connect your local Git repository to GitHub using SSH after your SSH key has been added to your account.

First, you test your SSH connection:

`ssh -T git@github.com`

If authentication works, GitHub confirms your username. That message means your computer can securely prove its identity using your private key.

Next, you copy your repository’s SSH URL from GitHub. It looks like:

`git@github.com:username/repository.git`

Then you connect your local project to that remote repository.

If you’re adding the remote for the first time:

`git remote add origin git@github.com:username/repository.git`

If a remote already exists and you want to switch it to SSH:

`git remote set-url origin git@github.com:username/repository.git`

After this, your local repository and GitHub are officially linked through SSH. From here on, `git push` and `git pull` communicate securely without passwords.

Conceptually, this step is about wiring your local history machine to a remote history server using cryptographic identity instead of credentials. Once connected, collaboration becomes frictionless—and frictionless systems are the ones teams actually use consistently.
