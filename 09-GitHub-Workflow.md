# GitHub Workflow

## Introduction

GitHub is more than just a place to store code. It provides a structured workflow that allows developers to collaborate on projects, track changes, review code, and safely merge contributions.

A typical GitHub workflow involves creating a repository, making changes locally using Git, and then sharing those changes through GitHub.

---

# Complete GitHub Workflow

The standard GitHub workflow looks like this:

```text
Create Repository on GitHub
            │
            ▼
Clone Repository
            │
            ▼
Create a New Branch
            │
            ▼
Make Changes
            │
            ▼
git add
            │
            ▼
git commit
            │
            ▼
git push
            │
            ▼
Open Pull Request
            │
            ▼
Code Review
            │
            ▼
Merge Pull Request
            │
            ▼
Update Local Repository
```

---

# Step 1: Create a Repository

The first step is to create a repository on GitHub.

A repository contains:

- Project files
- Commit history
- Branches
- Issues
- Pull Requests
- README
- Other project resources

Repositories can be either **Public** or **Private**.

---

# Step 2: Clone the Repository

To work on a repository, you first create a local copy using:

```bash
git clone https://github.com/username/project.git
```

Purpose:

- Downloads the complete repository.
- Copies all branches and commit history.
- Creates a local working directory.

---

# Step 3: Create a New Branch

Instead of working directly on the `main` branch, create a new branch.

Example:

```bash
git branch feature-login
```

or

```bash
git checkout -b feature-login
```

Modern Git:

```bash
git switch -c feature-login
```

Working in branches keeps the main branch stable while new features are being developed.

---

# Step 4: Make Changes

Edit your project files.

Example:

```
index.html

style.css

script.js
```

After making changes, check the repository status.

```bash
git status
```

---

# Step 5: Stage the Changes

Move modified files to the staging area.

```bash
git add .
```

Or stage a specific file.

```bash
git add index.html
```

---

# Step 6: Commit the Changes

Save the staged changes.

```bash
git commit -m "Add login page"
```

Always write meaningful commit messages that describe what changed.

---

# Step 7: Push the Branch

Upload your branch to GitHub.

```bash
git push origin feature-login
```

Now your branch is available on GitHub.

---

# Step 8: Open a Pull Request

A **Pull Request (PR)** is a request to merge your changes into another branch, usually `main`.

A Pull Request allows other developers to:

- Review your code.
- Suggest improvements.
- Discuss changes.
- Approve the work.

Only after approval are the changes merged into the main branch.

---

# Step 9: Code Review

During the review process, team members check:

- Code quality
- Readability
- Performance
- Bugs
- Security
- Coding standards

If improvements are needed, you make additional commits and push them to the same branch. The Pull Request updates automatically.

---

# Step 10: Merge the Pull Request

After the Pull Request is approved, it is merged into the target branch.

This combines your work with the main project.

After merging, the feature branch can usually be deleted.

---

# Step 11: Update Your Local Repository

After the project changes on GitHub, download the latest updates.

```bash
git pull origin main
```

This keeps your local repository synchronized with GitHub.

---

# GitHub Collaboration Example

Imagine three developers working on the same project.

```
Developer A → Login Feature

Developer B → Payment System

Developer C → User Profile
```

Each developer:

- Creates a separate branch.
- Works independently.
- Commits changes.
- Pushes the branch.
- Opens a Pull Request.

After review, all branches are merged into the `main` branch.

This allows multiple developers to work simultaneously without interfering with each other's work.

---

# Why Use Branches?

Working directly on the `main` branch can be risky.

Branches allow developers to:

- Develop new features safely.
- Fix bugs independently.
- Experiment without affecting the main project.
- Merge only tested code.

---

# Best Practices for GitHub Workflow

Follow these best practices:

- Pull the latest changes before starting work.
- Create a new branch for every feature or bug fix.
- Write clear commit messages.
- Push changes regularly.
- Open Pull Requests instead of committing directly to `main`.
- Review code carefully before merging.
- Delete feature branches after merging.
- Keep the `main` branch stable.

---

# Common Mistakes

### Working Directly on the Main Branch

Avoid making all changes directly on `main`.

Instead:

```
main

↓

feature-branch

↓

Pull Request

↓

Merge
```

---

### Forgetting to Pull

Before starting work, run:

```bash
git pull origin main
```

This ensures you have the latest version of the project.

---

### Poor Commit Messages

❌ Bad

```
Update
```

✅ Good

```
Add responsive navigation menu
```

---

### Large Pull Requests

Avoid combining many unrelated changes into a single Pull Request.

Smaller Pull Requests are easier to review and merge.

---

# GitHub Workflow Summary

```text
Create Repository
        │
        ▼
Clone Repository
        │
        ▼
Create Branch
        │
        ▼
Modify Files
        │
        ▼
git add
        │
        ▼
git commit
        │
        ▼
git push
        │
        ▼
Open Pull Request
        │
        ▼
Code Review
        │
        ▼
Merge
        │
        ▼
git pull
```

---

# Summary

In this chapter, you learned:

- How a typical GitHub workflow operates.
- How to clone a repository.
- Why branches are important.
- How to stage, commit, and push changes.
- What a Pull Request is and why it is used.
- The importance of code reviews.
- How branches are merged into the main project.
- Best practices for collaborating with GitHub.

By following this workflow, developers can work together efficiently, maintain high-quality code, and safely contribute to software projects of any size.
