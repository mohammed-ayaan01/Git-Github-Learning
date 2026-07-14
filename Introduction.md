# Linus Torvalds       --Linux Kernel(1991)    --Git(2005)

## Why is Git Around

--> Easily Recover Files
--> RoleBack to previously working state
--> To Control Version and reduce space

## Git vs GitHub

Git:
- Version control system.
- Works offline.
- Tracks changes locally.

GitHub:
- Cloud platform for hosting Git repositories.
- Used for collaboration and showcasing projects.

## History of Version Control Systems

1. Local Version Control Systems:
    --> Saved in Local Computer and can be lost easily
    --> Can RollBack and track files

2. Centralised Version Control Systems:
    --> Files are Pushed and Pulled through a Central Server

3. Distributed Version Control Systems(Git):
    --> Saves the Whole Repository as a Snapshot

## Features

1. Git Saves Snapshots not Differences

2. Git has Integrity (checksum)

3. Git generally only adds data

## Initial Set up

--> Check if Git is already installed:
```
git --version
```

--> Installation:

**Windows:**
- Download from https://git-scm.com/download/win
- Run installer (default options are fine for beginners)
- Verify with: `git --version` (in Git Bash or CMD)

**macOS:** (reference only — I use Windows/Linux, verified via official docs)
- Option 1: Install via Homebrew
```
brew install git
```
- Option 2: Install Xcode Command Line Tools (includes Git)
```
xcode-select --install
```
- Option 3: Download installer from https://git-scm.com/download/mac

**Linux (Debian/Ubuntu):**
```
sudo apt update
sudo apt install git
```

**Linux (Fedora/RHEL):**
```
sudo dnf install git
```

--> First-time Configuration (do this once per machine):
```
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"
```
- This info gets attached to every commit you make
- Applies to ALL repos on this machine, not just one

--> Check your config anytime:
```
git config --global --list
```

--> (Optional) Set default branch name to 'main':
```
git config --global init.defaultBranch main
```

--> (Optional) Set default editor for commit messages:
```
git config --global core.editor "code --wait"   # if using VS Code
```