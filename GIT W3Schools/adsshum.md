# Connecting to GitHub via SSH

SSH authentication replaces passwords with cryptography. When you generate an SSH key pair, you get two mathematically linked files: a **private key** (stays on your machine, never shared) and a **public key** (safe to distribute). GitHub stores your public key, and when you connect, your machine proves it holds the matching private key — without ever transmitting it. GitHub recognises you by that proof alone.

-----

## Setup Flow

### 1. Generate your key pair and add it to the SSH agent

```bash
ssh-keygen -t ed25519 -C "your@email.com"
ssh-add ~/.ssh/id_ed25519
```

The agent holds your private key in memory so you don’t re-enter your passphrase every session.

### 2. Copy your public key

The command varies by OS:

|OS                |Command                                  |
|------------------|-----------------------------------------|
|macOS             |`pbcopy < ~/.ssh/id_ed25519.pub`         |
|Linux             |`xclip -sel clip < ~/.ssh/id_ed25519.pub`|
|Windows (Git Bash)|`clip < ~/.ssh/id_ed25519.pub`           |

### 3. Add the key to GitHub

**Profile → Settings → SSH and GPG Keys → New SSH Key** → paste and confirm with your password or 2FA.

Once saved, GitHub associates that public key with your account. Any machine holding the corresponding private key is implicitly trusted as you.

-----

## Why This Matters

Use SSH URLs for all push/pull/clone operations:

```
git@github.com:username/repo.git
```

No password prompts, no token management, no expiry headaches. The handshake is automatic and the security model is stronger — an attacker would need your private key file *and* your passphrase, rather than just a stolen password or token.

> This is the standard professional setup because it’s both more secure and more ergonomic than any password-based alternative.