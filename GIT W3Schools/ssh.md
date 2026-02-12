### What SSH Is

SSH (Secure Shell) is a secure way to connect to remote systems, including Git hosting platforms like GitHub, GitLab, and Bitbucket. Instead of typing your username and password every time, SSH uses cryptographic keys to prove your identity.

---

### How SSH Keys Work

SSH uses a **key pair**:

* **Public key** → Shared with the server (like giving someone a lock).
* **Private key** → Kept secret on your computer (the only key that opens the lock).

If the server recognizes your public key and you have the matching private key, access is granted. No password required.

The private key must never be shared. If it’s exposed, you generate a new pair immediately.

---

### Setting Up SSH (First Time)

1. Start the SSH agent (a background process that manages keys).
2. Generate a key pair using `ssh-keygen`.
3. Add your private key to the SSH agent with `ssh-add`.
4. Copy your public key and paste it into your Git hosting account settings.
5. Test the connection using `ssh -T git@github.com` (or the equivalent platform).

Once configured, Git operations like push and pull can run securely over SSH.

---

### Managing SSH Keys

* `ssh-add -l` → List loaded keys
* `ssh-add -d` → Remove a key from the agent

If you get “Permission denied,” common causes include:

* Public key not added to your Git account
* Private key not loaded into the agent
* Incorrect file permissions
* Using the wrong remote URL (should start with `git@` for SSH)

---

### Security Best Practices

Use a passphrase for extra protection.
Keep private key permissions restricted.
Never share your private key.
Regenerate keys if compromised.
