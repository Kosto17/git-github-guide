# Core Git Workflow

## Introduction

Git follows a simple workflow to track and manage changes in a project. Every time you create or modify a project, you use a series of Git commands to save your work and upload it to GitHub.

Understanding this workflow is essential because these are the commands you will use almost every day as a developer.

---

# Complete Git Workflow

```text
Create Project
      │
      ▼
git init
      │
      ▼
git status
      │
      ▼
Create or Modify Files
      │
      ▼
git add
      │
      ▼
git commit
      │
      ▼
git remote add origin
      │
      ▼
git branch -M main
      │
      ▼
git push -u origin main
      │
      ▼
Project Uploaded to GitHub
```

---

# Step 1: Create a Project

First, create a folder for your project.

Example:

```text
My-Portfolio/
```

Move into the project folder using:

```bash
cd My-Portfolio
```

---

# Step 2: Initialize Git Repository

Command:

```bash
git init
```

Purpose:

Initializes a new Git repository in the current folder.

When this command is executed, Git creates a hidden folder named `.git`.

This folder stores:

- Commit history
- Branch information
- Configuration
- Project metadata

Example:

```bash
git init
```

Output:

```text
Initialized empty Git repository in C:/Users/Krish/My-Portfolio/.git/
```

---

# Step 3: Check Repository Status

Command:

```bash
git status
```

Purpose:

Displays the current status of your repository.

It tells you:

- Current branch
- Modified files
- New files
- Deleted files
- Files ready to commit

Example:

```bash
git status
```

Possible Output:

```text
On branch main

No commits yet

Untracked files:
    index.html

nothing added to commit
```

---

# Step 4: Create or Modify Files

Create your project files.

Example:

```text
index.html
style.css
script.js
README.md
```

Git now detects these files as **Untracked Files**.

Check using:

```bash
git status
```

---

# Step 5: Stage Files

Before saving changes permanently, Git requires you to move them to the **Staging Area**.

Stage one file:

```bash
git add index.html
```

Stage multiple files:

```bash
git add index.html style.css
```

Stage every file:

```bash
git add .
```

Purpose:

Moves selected files into the Staging Area.

---

# Step 6: Check Status Again

Run:

```bash
git status
```

Output:

```text
Changes to be committed:
    new file: index.html
```

This confirms that Git is ready to create a commit.

---

# Step 7: Create a Commit

Command:

```bash
git commit -m "Initial commit"
```

Purpose:

Creates a permanent snapshot of your project.

The message should briefly describe the changes.

Good examples:

```text
Initial commit

Add login page

Fix navigation bar

Update README
```

Avoid messages like:

```text
Changes

Update

abc

Done
```

---

# Step 8: Create a Repository on GitHub

Go to GitHub and create a new repository.

Example:

```
My-Portfolio
```

Do not add:

- README
- .gitignore
- License

(if your local project already contains them)

---

# Step 9: Connect Local Repository to GitHub

Command:

```bash
git remote add origin https://github.com/username/My-Portfolio.git
```

Purpose:

Connects your local Git repository with the remote GitHub repository.

Verify the connection:

```bash
git remote -v
```

Output:

```text
origin https://github.com/username/My-Portfolio.git (fetch)

origin https://github.com/username/My-Portfolio.git (push)
```

---

# Step 10: Rename the Default Branch

Command:

```bash
git branch -M main
```

Purpose:

Renames the current branch to **main**.

Most modern Git repositories use **main** as the default branch.

---

# Step 11: Push the Project to GitHub

Command:

```bash
git push -u origin main
```

Purpose:

Uploads your commits to GitHub.

Explanation:

- `push` → Upload changes
- `-u` → Set upstream branch
- `origin` → Remote repository
- `main` → Branch name

The `-u` option only needs to be used once. After that, you can simply use:

```bash
git push
```

---

# Making Future Changes

After your project is on GitHub, your daily workflow becomes:

Modify files

↓

```bash
git status
```

↓

```bash
git add .
```

↓

```bash
git commit -m "Describe your changes"
```

↓

```bash
git push
```

---

# Complete Workflow Example

```bash
mkdir My-Portfolio

cd My-Portfolio

git init

git status

git add .

git commit -m "Initial commit"

git remote add origin https://github.com/username/My-Portfolio.git

git branch -M main

git push -u origin main
```

---

# Workflow Diagram

```text
Working Directory
        │
        ▼
git add
        │
        ▼
Staging Area
        │
        ▼
git commit
        │
        ▼
Local Repository
        │
        ▼
git push
        │
        ▼
GitHub Repository
```

---

# Common Mistakes

### Forgetting `git add`

If you commit without staging files, Git will say:

```text
nothing to commit
```

---

### Forgetting Commit Message

Every commit should include a meaningful message.

Example:

```bash
git commit -m "Fix login validation"
```

---

### Incorrect Repository URL

Always copy the repository URL directly from GitHub.

---

### Pushing Before Committing

Git only pushes committed changes.

Always follow:

```text
git add

↓

git commit

↓

git push
```

---

# Summary

In this chapter, you learned:

- How to initialize a Git repository.
- How to check repository status.
- How to stage files.
- How to create commits.
- How to connect a local repository to GitHub.
- How to push code to GitHub.
- The complete Git workflow from project creation to online repository.
- Common mistakes beginners should avoid.

You can now create a project, track changes with Git, and upload it to GitHub using the standard workflow followed by developers worldwide.
