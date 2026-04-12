# Git and GitHub Workflow Guide

An easy, practical, and copy-ready GitHub workflow guide with clear command info, branching workflow, and merge conflict resolution from A to Z.

[![GitHub Repo](https://img.shields.io/badge/GitHub-Workflow%20Guide-181717?logo=github)](https://github.com/zafar1162014/GitHub-Workflow-Guide)
[![Git](https://img.shields.io/badge/Git-Cheat%20Sheet-F05032?logo=git&logoColor=white)](https://git-scm.com/doc)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

Repository: https://github.com/zafar1162014/GitHub-Workflow-Guide  
Author: Muhammad Zafar Ul Haq

---

## Why This Guide

- Beginner-friendly and easy to scan.
- Every command has a clear explanation.
- All commands are copy-ready.
- Covers daily workflow, branching, and conflict handling.

## Quick Navigation

- [Installation](#installation)
- [Git Setup](#git-setup)
- [SSH Setup for GitHub](#ssh-setup-for-github)
- [Quick Start Workflow](#quick-start-workflow)
- [Create and Clone Repositories](#create-and-clone-repositories)
- [Daily Git Commands](#daily-git-commands)
- [Inspect and Compare Changes](#inspect-and-compare-changes)
- [Undo and Restore](#undo-and-restore)
- [Branching and Merging](#branching-and-merging)
- [Sharing and Syncing with Remote](#sharing-and-syncing-with-remote)
- [Extra Useful Commands](#extra-useful-commands)
- [In-Depth Feature Workflow](#in-depth-feature-workflow)
- [Merge Conflict Resolution (A to Z)](#merge-conflict-resolution-a-to-z)
- [Learning Resource](#learning-resource)

---

## Installation

- Git download: https://git-scm.com/downloads
- GitHub Desktop: https://desktop.github.com/
- Official docs: https://git-scm.com/doc

## Git Setup

### Command Info and Copy

Set your name for commit history.

```bash
git config --global user.name "<username>"
```

Set your email for commit history.

```bash
git config --global user.email <email address>
```

## SSH Setup for GitHub

### Command Info and Copy

Generate a new SSH key (recommended: ed25519).

```bash
ssh-keygen -t ed25519 -C "<your-email@example.com>"
```

If your system does not support ed25519, use RSA instead.

```bash
ssh-keygen -t rsa -b 4096 -C "<your-email@example.com>"
```

Start the SSH agent.

```bash
eval "$(ssh-agent -s)"
```

Add your SSH private key to the agent.

```bash
ssh-add ~/.ssh/id_ed25519
```

If you created RSA key, add this key instead.

```bash
ssh-add ~/.ssh/id_rsa
```

Copy your public key and add it to GitHub:
GitHub -> Settings -> SSH and GPG keys -> New SSH key

```bash
cat ~/.ssh/id_ed25519.pub
```

If you created RSA key, copy this public key.

```bash
cat ~/.ssh/id_rsa.pub
```

Confirm key is loaded in the agent.

```bash
ssh-add -l
```

Test SSH connection with GitHub.

```bash
ssh -T git@github.com
```

Clone a repository over SSH after your key is set up.

```bash
git clone ssh://git@github.com/<username>/<repository-name>.git
```

## Quick Start Workflow

Clone a repo, create a feature branch, commit changes, and push branch to GitHub.

```bash
git clone ssh://git@github.com/<username>/<repository-name>.git
cd <repository-name>
git checkout -b feature/<short-name>
git add -A
git commit -m "feat: add <change>"
git push -u origin feature/<short-name>
```

## Create and Clone Repositories

### Command Info and Copy

Start Git tracking in current folder.

```bash
git init
```

Download a remote repository to your machine.

```bash
git clone ssh://git@github.com/<username>/<repository-name>.git
```

## Daily Git Commands

### Command Info and Copy

Check changed, staged, and untracked files.

```bash
git status
```

Stage one specific file.

```bash
git add <file-name.txt>
```

Stage all changes in the repository.

```bash
git add -A
```

Alternative to stage all changes.

```bash
git add .
```

Save staged changes with a message.

```bash
git commit -m "<commit message>"
```

Remove file/folder and stage the deletion.

```bash
git rm -r <file-name.txt>
```

## Inspect and Compare Changes

### Command Info and Copy

Show commit history.

```bash
git log
```

Show history with more summary details.

```bash
git log --summary
```

Show short one-line history.

```bash
git log --oneline
```

Show one-line history with pretty format.

```bash
git log --pretty=oneline
```

Show compact short history format.

```bash
git log --pretty=short
```

## Undo and Restore

### Command Info and Copy

Quickly list commits.

```bash
git log --oneline
```

Checkout a past commit.

```bash
git checkout <commit id>
```

Undo a commit safely with a new commit.

```bash
git revert <commit id>
```

Reset history and working tree to a commit.

```bash
git reset --hard <commit id>
```

Stop tracking a file/folder but keep it locally.

```bash
git rm --cached <file/folder>
```

Restore a file to Git version.

```bash
git checkout <file/to/restore>
```

## Branching and Merging

### Command Info and Copy

Show local branches.

```bash
git branch
```

Show local and remote branches.

```bash
git branch -a
```

Create a new branch.

```bash
git branch <branch name>
```

Create and switch to a new branch.

```bash
git checkout -b <branch name>
```

Create local branch from a remote branch.

```bash
git checkout -b <branch name> origin/<branch name>
```

Rename a branch.

```bash
git branch -m <old branch name> <new branch name>
```

Switch to a branch.

```bash
git checkout <branch name>
```

Switch back to previously checked out branch.

```bash
git checkout -
```

Discard local changes in one file.

```bash
git checkout -- <file-name.txt>
```

Delete local branch safely.

```bash
git branch -d <branch name>
```

Delete remote branch.

```bash
git push origin --delete <branch name>
```

Compare changes between two branches.

```bash
git diff <source branch> <target branch>
```

Merge branch into current branch.

```bash
git merge <branch name>
```

Merge source branch into target branch.

```bash
git merge <source branch> <target branch>
```

Save uncommitted changes temporarily.

```bash
git stash
```

Remove all stash entries.

```bash
git stash clear
```

## Sharing and Syncing with Remote

### Command Info and Copy

Push branch to remote repository.

```bash
git push origin <branch name>
```

Push and set upstream tracking.

```bash
git push -u origin <branch name>
```

Push current tracked branch.

```bash
git push
```

Push all local branches.

```bash
git push --all
```

Force push (use carefully).

```bash
git push -f
```

Delete branch from remote.

```bash
git push origin --delete <branch name>
```

Pull latest updates from tracked branch.

```bash
git pull
```

Pull updates from specific branch.

```bash
git pull origin <branch name>
```

Add remote named origin.

```bash
git remote add origin ssh://git@github.com/<username>/<repository-name>.git
```

Change origin URL to SSH URL.

```bash
git remote set-url origin ssh://git@github.com/<username>/<repository-name>.git
```

## Extra Useful Commands

### Command Info and Copy

Show remote URLs and confirm SSH/HTTPS origin.

```bash
git remote -v
```

Download latest remote updates without merging.

```bash
git fetch origin
```

Switch branches using modern Git command.

```bash
git switch <branch name>
```

Create and switch branch using modern Git command.

```bash
git switch -c <branch name>
```

Restore file changes in working tree.

```bash
git restore <file-name.txt>
```

Show stash entries.

```bash
git stash list
```

Apply and remove latest stash entry.

```bash
git stash pop
```
Restore a file to Git version.

```bash
git checkout <file/to/restore>
```

## In-Depth Feature Workflow

### 1. Sync Main Before Starting

Always start feature work from latest `main`.

```bash
git checkout main
git pull origin main
```

### 2. Create and Start Feature Branch

Isolate your work in a separate branch.

```bash
git checkout -b feature/<short-name>
```

### 3. Commit in Small Units

Keep history clean and review-friendly.

```bash
git status
git add -A
git commit -m "feat: implement <small change>"
```

### 4. Publish Branch and Open Pull Request

Share your branch and open PR for review.

```bash
git push -u origin feature/<short-name>
```

### 5. Keep Feature Branch Updated

Reduce large conflicts before merge.

```bash
git checkout main
git pull origin main
git checkout feature/<short-name>
git merge main
```

### 6. After Merge, Clean Up

Keep local and remote branches tidy.

```bash
git checkout main
git pull origin main
git branch -d feature/<short-name>
git push origin --delete feature/<short-name>
```

## Merge Conflict Resolution (A to Z)

### Command Info and Copy

Show which files are in conflict.

```bash
git status
```

List unresolved conflict files only.

```bash
git diff --name-only --diff-filter=U
```

Inspect conflict details.

```bash
git diff
```

Show commits involved in current conflict.

```bash
git log --merge --oneline
```

Accept your current branch version for one file.

```bash
git checkout --ours <file>
```

Accept incoming branch version for one file.

```bash
git checkout --theirs <file>
```

Open visual merge tool.

```bash
git mergetool
```

Mark file as resolved.

```bash
git add <file>
```

Finalize merge conflict resolution.

```bash
git commit -m "resolve: merge conflicts"
```

Cancel current merge.

```bash
git merge --abort
```

Continue rebase after resolving conflicts.

```bash
git rebase --continue
```

Skip problematic patch during rebase.

```bash
git rebase --skip
```

Cancel current rebase.

```bash
git rebase --abort
```

### Merge Conflict Fast Flow

Resolve merge conflict quickly when you already know what to keep.

```bash
git status
git diff --name-only --diff-filter=U
git diff
git add <file1> <file2>
git commit -m "resolve: merge conflicts"
```

### Rebase Conflict Fast Flow

Resolve and continue rebase process.

```bash
git status
git diff --name-only --diff-filter=U
git add <file1> <file2>
git rebase --continue
```

## Learning Resource

- GitHub Education cheat sheet (PDF): https://education.github.com/git-cheat-sheet-education.pdf

---

If this guide helped you, star the repo and share it with your team.
