# Git and GitHub Workflow Guide

An easy, practical, and copy-ready GitHub workflow guide with Git commands, branching, pull request flow, and merge conflict resolution from A to Z.

[![GitHub Repo](https://img.shields.io/badge/GitHub-Workflow%20Guide-181717?logo=github)](https://github.com/zafar1162014/GitHub-Workflow-Guide)
[![Git](https://img.shields.io/badge/Git-Cheat%20Sheet-F05032?logo=git&logoColor=white)](https://git-scm.com/doc)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

Repository: https://github.com/zafar1162014/GitHub-Workflow-Guide  
Author: Muhammad Zafar Ul Haq

---

## Why This Guide

- Beginner-friendly and fast to scan.
- Useful for developers, students, and teams.
- Includes real workflow steps, not just isolated commands.
- Covers merge/rebase conflict handling in detail.

## Quick Navigation

- [Installation](#installation)
- [Git Setup](#git-setup)
- [Quick Start Workflow](#quick-start-workflow)
- [Create and Clone Repositories](#create-and-clone-repositories)
- [Daily Git Commands](#daily-git-commands)
- [Branching and Merging](#branching-and-merging)
- [Sharing and Syncing with Remote](#sharing-and-syncing-with-remote)
- [Inspect and Compare Changes](#inspect-and-compare-changes)
- [Undo and Restore](#undo-and-restore)
- [In-Depth Feature Workflow](#in-depth-feature-workflow)
- [Merge Conflict Resolution (A to Z)](#merge-conflict-resolution-a-to-z)
- [Copy-Ready Command Bundles](#copy-ready-command-bundles)
- [SEO and Repository Visibility Tips](#seo-and-repository-visibility-tips)
- [Learning Resource](#learning-resource)

---

## Installation

- Git download: https://git-scm.com/downloads
- GitHub Desktop: https://desktop.github.com/
- Official Git docs: https://git-scm.com/doc

## Git Setup

| Description | Command |
| --- | --- |
| Configure author name | `git config --global user.name "<username>"` |
| Configure author email | `git config --global user.email <email address>` |

### Individual Copy Commands

```bash
git config --global user.name "<username>"
```

```bash
git config --global user.email <email address>
```

## Quick Start Workflow

```bash
git clone ssh://git@github.com/<username>/<repository-name>.git
cd <repository-name>
git checkout -b feature/<short-name>
git add -A
git commit -m "feat: add <change>"
git push -u origin feature/<short-name>
```

## Create and Clone Repositories

| Description | Command |
| --- | --- |
| Initialize local repository | `git init` |
| Clone repository via SSH | `git clone ssh://git@github.com/<username>/<repository-name>.git` |

### Individual Copy Commands

```bash
git init
```

```bash
git clone ssh://git@github.com/<username>/<repository-name>.git
```

## Daily Git Commands

| Description | Command |
| --- | --- |
| Check status | `git status` |
| Stage one file | `git add <file-name.txt>` |
| Stage all changes | `git add -A` or `git add .` |
| Commit changes | `git commit -m "<commit message>"` |
| Remove file/folder | `git rm -r <file-name.txt>` |

### Individual Copy Commands

```bash
git status
```

```bash
git add <file-name.txt>
```

```bash
git add -A
```

```bash
git add .
```

```bash
git commit -m "<commit message>"
```

```bash
git rm -r <file-name.txt>
```

## Branching and Merging

| Description | Command |
| --- | --- |
| List local branches | `git branch` |
| List local and remote branches | `git branch -a` |
| Create new branch | `git branch <branch name>` |
| Create and switch branch | `git checkout -b <branch name>` |
| Track remote branch locally | `git checkout -b <branch name> origin/<branch name>` |
| Rename branch | `git branch -m <old branch name> <new branch name>` |
| Switch branch | `git checkout <branch name>` |
| Switch to last branch | `git checkout -` |
| Discard file changes | `git checkout -- <file-name.txt>` |
| Delete local branch | `git branch -d <branch name>` |
| Delete remote branch | `git push origin --delete <branch name>` |
| Diff before merge | `git diff <source branch> <target branch>` |
| Merge into current branch | `git merge <branch name>` |
| Merge source into target | `git merge <source branch> <target branch>` |
| Stash current work | `git stash` |
| Clear all stash entries | `git stash clear` |

### Individual Copy Commands

```bash
git branch
```

```bash
git branch -a
```

```bash
git branch <branch name>
```

```bash
git checkout -b <branch name>
```

```bash
git checkout -b <branch name> origin/<branch name>
```

```bash
git branch -m <old branch name> <new branch name>
```

```bash
git checkout <branch name>
```

```bash
git checkout -
```

```bash
git checkout -- <file-name.txt>
```

```bash
git branch -d <branch name>
```

```bash
git push origin --delete <branch name>
```

```bash
git diff <source branch> <target branch>
```

```bash
git merge <branch name>
```

```bash
git merge <source branch> <target branch>
```

```bash
git stash
```

```bash
git stash clear
```

## Sharing and Syncing with Remote

| Description | Command |
| --- | --- |
| Push branch | `git push origin <branch name>` |
| Push and set upstream | `git push -u origin <branch name>` |
| Push current tracked branch | `git push` |
| Push all branches | `git push --all` |
| Force push | `git push -f` |
| Delete remote branch | `git push origin --delete <branch name>` |
| Pull latest tracked branch | `git pull` |
| Pull specific branch | `git pull origin <branch name>` |
| Add remote origin | `git remote add origin ssh://git@github.com/<username>/<repository-name>.git` |
| Switch origin to SSH URL | `git remote set-url origin ssh://git@github.com/<username>/<repository-name>.git` |

### Individual Copy Commands

```bash
git push origin <branch name>
```

```bash
git push -u origin <branch name>
```

```bash
git push
```

```bash
git push --all
```

```bash
git push -f
```

```bash
git push origin --delete <branch name>
```

```bash
git pull
```

```bash
git pull origin <branch name>
```

```bash
git remote add origin ssh://git@github.com/<username>/<repository-name>.git
```

```bash
git remote set-url origin ssh://git@github.com/<username>/<repository-name>.git
```

## Inspect and Compare Changes

| Description | Command |
| --- | --- |
| Commit history | `git log` |
| Detailed history | `git log --summary` |
| One-line history | `git log --oneline` |
| Alternative one-line style | `git log --pretty=oneline` |
| Short style history | `git log --pretty=short` |

### Individual Copy Commands

```bash
git log
```

```bash
git log --summary
```

```bash
git log --oneline
```

```bash
git log --pretty=oneline
```

```bash
git log --pretty=short
```

## Undo and Restore

| Description | Command |
| --- | --- |
| List commits quickly | `git log --oneline` |
| Checkout old commit | `git checkout <commit id>` |
| Revert a commit safely | `git revert <commit id>` |
| Hard reset to commit | `git reset --hard <commit id>` |
| Stop tracking file/folder | `git rm --cached <file/folder>` |
| Restore file from Git | `git checkout <file/to/restore>` |

### Individual Copy Commands

```bash
git log --oneline
```

```bash
git checkout <commit id>
```

```bash
git revert <commit id>
```

```bash
git reset --hard <commit id>
```

```bash
git rm --cached <file/folder>
```

```bash
git checkout <file/to/restore>
```

## In-Depth Feature Workflow

### 1. Sync Main Before Starting

```bash
git checkout main
git pull origin main
```

### 2. Create and Start Feature Branch

```bash
git checkout -b feature/<short-name>
```

### 3. Commit in Small Units

```bash
git status
git add -A
git commit -m "feat: implement <small change>"
```

### 4. Publish Branch and Open Pull Request

```bash
git push -u origin feature/<short-name>
```

### 5. Keep Feature Branch Updated

```bash
git checkout main
git pull origin main
git checkout feature/<short-name>
git merge main
```

### 6. After Merge, Clean Up

```bash
git checkout main
git pull origin main
git branch -d feature/<short-name>
git push origin --delete feature/<short-name>
```

## Merge Conflict Resolution (A to Z)

| Step | Command |
| --- | --- |
| Show conflict status | `git status` |
| List unresolved files | `git diff --name-only --diff-filter=U` |
| View conflict details | `git diff` |
| Show conflict-related commits | `git log --merge --oneline` |
| Keep current branch version | `git checkout --ours <file>` |
| Keep incoming branch version | `git checkout --theirs <file>` |
| Open visual merge tool | `git mergetool` |
| Mark resolved file | `git add <file>` |
| Finalize merge conflict resolution | `git commit -m "resolve: merge conflicts"` |
| Abort merge | `git merge --abort` |
| Continue rebase | `git rebase --continue` |
| Skip one patch in rebase | `git rebase --skip` |
| Abort rebase | `git rebase --abort` |

### Individual Copy Commands

```bash
git status
```

```bash
git diff --name-only --diff-filter=U
```

```bash
git diff
```

```bash
git log --merge --oneline
```

```bash
git checkout --ours <file>
```

```bash
git checkout --theirs <file>
```

```bash
git mergetool
```

```bash
git add <file>
```

```bash
git commit -m "resolve: merge conflicts"
```

```bash
git merge --abort
```

```bash
git rebase --continue
```

```bash
git rebase --skip
```

```bash
git rebase --abort
```

### Merge Conflict Fast Flow

```bash
git status
git diff --name-only --diff-filter=U
git diff
git add <file1> <file2>
git commit -m "resolve: merge conflicts"
```

### Rebase Conflict Fast Flow

```bash
git status
git diff --name-only --diff-filter=U
git add <file1> <file2>
git rebase --continue
```

## Copy-Ready Command Bundles

### Setup Identity

```bash
git config --global user.name "<username>"
git config --global user.email <email address>
```

### Create or Clone Project

```bash
git init
git clone ssh://git@github.com/<username>/<repository-name>.git
```

### Daily Workflow

```bash
git status
git add -A
git commit -m "<commit message>"
git push
```

### Branch Workflow

```bash
git branch <branch name>
git checkout -b <branch name>
git checkout <branch name>
git merge <branch name>
```

### Update from Remote

```bash
git pull
git pull origin <branch name>
```

### Remote Setup and Push

```bash
git remote add origin ssh://git@github.com/<username>/<repository-name>.git
git push -u origin <branch name>
```

### Undo and Restore

```bash
git log --oneline
git revert <commit id>
git reset --hard <commit id>
git rm --cached <file/folder>
git checkout <file/to/restore>
```

## SEO and Repository Visibility Tips

To help this repository rank higher in search results on GitHub and Google:

- Keep repository name and README title aligned with target keywords:
  Git, GitHub, workflow, cheatsheet, merge conflict, branching.
- Add topics in GitHub repository settings:
  `git`, `github`, `git-workflow`, `git-cheatsheet`, `version-control`, `merge-conflicts`.
- Keep README updated regularly with practical examples.
- Add a short demo screenshot or GIF in the repository root.
- Encourage stars and forks by sharing the repository in developer communities.

## Learning Resource

- GitHub Education cheat sheet (PDF): https://education.github.com/git-cheat-sheet-education.pdf

---

If this guide helped you, star the repo and share it with your team.
