# Commits and Commit Messages

## Introduction

A **commit** is one of the most important concepts in Git. Every time you commit, Git saves a snapshot of your project at that moment.

Think of a commit as a **checkpoint** in a video game. If something goes wrong later, you can return to that checkpoint instead of starting over.

Each commit becomes a permanent part of your project's history.

---

# What is a Commit?

A commit is a recorded snapshot of all staged changes in your project.

When you commit, Git stores:

- The current state of the project
- The changes made
- The author's name
- The author's email
- Date and time
- Commit message
- A unique Commit Hash

Example:

```bash
git commit -m "Add login page"
```

Git creates a new snapshot of your project.

---

# Why Are Commits Important?

Commits help developers:

- Save project progress.
- Track every change.
- Restore previous versions.
- Understand what changed.
- Collaborate with teams.
- Debug problems more easily.

Without commits, it would be difficult to know when or why changes were made.

---

# How Commits Work

Suppose you create a website.

### Initial Project

```
index.html
style.css
```

↓

Stage the files

```bash
git add .
```

↓

Create the first commit

```bash
git commit -m "Initial commit"
```

Git saves the first version.

---

Later, you add:

```
script.js
```

↓

Again

```bash
git add .
```

↓

```bash
git commit -m "Add JavaScript functionality"
```

Git now stores another snapshot.

The project history becomes:

```
Commit 2
↓

Commit 1
```

Each commit
