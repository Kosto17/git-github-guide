# Common Git Commands

## Introduction

Git provides many commands to help developers manage projects efficiently. Some commands are used daily, while others are used for specific situations such as viewing history, switching branches, or restoring files.

This chapter covers the most commonly used Git commands along with their purpose, syntax, examples, and usage.

---

# 1. git init

### Purpose

Initializes a new Git repository.

### Syntax

```bash
git init
```

### Example

```bash
git init
```

### Description

Creates a hidden `.git` folder that stores all version history and repository information.

---

# 2. git status

### Purpose

Displays the current state of the repository.

### Syntax

```bash
git status
```

### Example

```bash
git status
```

### Description

Shows:

- Current branch
- Modified files
- Untracked files
- Staged files

---

# 3. git add

### Purpose

Stages files before committing.

### Syntax

```bash
git add <filename>
```

### Example

```bash
git add index.html
```

### Description

Adds a specific file to the staging area.

---

# 4. git add .

### Purpose

Stages all modified and new files.

### Syntax

```bash
git add .
```

### Example

```bash
git add .
```

### Description

Stages every change in the current directory.

---

# 5. git commit

### Purpose

Creates a snapshot of staged changes.

### Syntax

```bash
git commit -m "Commit message"
```

### Example

```bash
git commit -m "Add login page"
```

### Description

Saves changes permanently in the local repository.

---

# 6. git log

### Purpose

Displays commit history.

### Syntax

```bash
git log
```

### Example

```bash
git log
```

### Description

Shows:

- Commit hash
- Author
- Date
- Commit message

---

# 7. git log --oneline

### Purpose

Displays a short version of commit history.

### Syntax

```bash
git log --oneline
```

### Example

```bash
git log --oneline
```

### Description

Shows each commit in a single line.

---

# 8. git diff

### Purpose

Shows changes between file versions.

### Syntax

```bash
git diff
```

### Example

```bash
git diff
```

### Description

Compares modified files with the last committed version.

---

# 9. git clone

### Purpose

Downloads an existing repository.

### Syntax

```bash
git clone <repository-url>
```

### Example

```bash
git clone https://github.com/username/project.git
```

### Description

Creates a complete local copy of a remote repository.

---

# 10. git remote -v

### Purpose

Shows connected remote repositories.

### Syntax

```bash
git remote -v
```

### Example

```bash
git remote -v
```

### Description

Displays the remote repository URLs for fetching and pushing.

---

# 11. git remote add origin

### Purpose

Connects a local repository to a remote repository.

### Syntax

```bash
git remote add origin <repository-url>
```

### Example

```bash
git remote add origin https://github.com/username/project.git
```

### Description

Adds a remote named `origin`.

---

# 12. git push

### Purpose

Uploads commits to a remote repository.

### Syntax

```bash
git push
```

### First Push

```bash
git push -u origin main
```

### Description

Transfers committed changes from the local repository to GitHub.

---

# 13. git pull

### Purpose

Downloads and merges the latest changes.

### Syntax

```bash
git pull
```

### Example

```bash
git pull origin main
```

### Description

Keeps your local repository up to date.

---

# 14. git fetch

### Purpose

Downloads remote changes without merging them.

### Syntax

```bash
git fetch
```

### Example

```bash
git fetch origin
```

### Description

Lets you review updates before merging them.

---

# 15. git branch

### Purpose

Displays or creates branches.

### Syntax

```bash
git branch
```

### Example

```bash
git branch feature-login
```

### Description

Creates or lists branches in the repository.

---

# 16. git checkout

### Purpose

Switches to another branch.

### Syntax

```bash
git checkout <branch-name>
```

### Example

```bash
git checkout feature-login
```

### Description

Moves your working directory to another branch.

---

# 17. git switch

### Purpose

Switches branches using the modern Git command.

### Syntax

```bash
git switch <branch-name>
```

### Example

```bash
git switch main
```

### Description

A newer and simpler alternative to `git checkout` for switching branches.

---

# 18. git merge

### Purpose

Combines changes from one branch into another.

### Syntax

```bash
git merge <branch-name>
```

### Example

```bash
git merge feature-login
```

### Description

Merges the specified branch into the current branch.

---

# 19. git restore

### Purpose

Restores files to a previous state.

### Syntax

```bash
git restore <filename>
```

### Example

```bash
git restore index.html
```

### Description

Discards unwanted changes in a file before it is committed.

---

# 20. git reset

### Purpose

Unstages files or moves the repository to an earlier commit.

### Syntax

```bash
git reset
```

### Example

```bash
git reset HEAD index.html
```

### Description

Removes files from the staging area without deleting your work.

---

# 21. git stash

### Purpose

Temporarily saves uncommitted changes.

### Syntax

```bash
git stash
```

### Example

```bash
git stash
```

### Description

Stores unfinished work so you can switch branches without committing.

Restore the stashed changes:

```bash
git stash pop
```

---

# Quick Command Summary

| Command | Purpose |
|----------|----------|
| `git init` | Initialize repository |
| `git status` | Check repository status |
| `git add` | Stage selected files |
| `git add .` | Stage all files |
| `git commit -m` | Save changes |
| `git log` | View commit history |
| `git diff` | Compare changes |
| `git clone` | Download repository |
| `git remote -v` | View remote repository |
| `git push` | Upload commits |
| `git pull` | Download and merge changes |
| `git fetch` | Download changes only |
| `git branch` | Manage branches |
| `git checkout` | Switch branches |
| `git switch` | Modern branch switching |
| `git merge` | Merge branches |
| `git restore` | Restore files |
| `git reset` | Unstage or reset changes |
| `git stash` | Temporarily save changes |

---

# Summary

In this chapter, you learned the most commonly used Git commands, their purpose, syntax, examples, and when to use them. These commands form the foundation of daily Git usage and will help you manage repositories, track changes, collaborate with others, and maintain project history efficiently.
