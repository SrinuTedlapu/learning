# 🌿 Git Branching - Detailed Guide

Branching in Git is a powerful feature that lets you work on multiple versions of a project simultaneously. It allows safe experimentation and development without affecting the main codebase.

---

## 🔰 What is a Branch?

A branch in Git is a movable pointer to a commit. It enables parallel development — for example, one branch can contain a new feature while the main branch remains stable.

---

## 📌 Why Use Branches?

- Isolate features or fixes
- Collaborate without interfering with others
- Experiment freely
- Maintain a stable `main` or `production` branch

---

## 🛠️ Common Branching Commands

### Create a New Branch

```bash
git branch feature-login
```

Creates a branch named `feature-login`.

### Switch to a Branch

```bash
git checkout feature-login
```

Moves to the `feature-login` branch.

### Create and Switch in One Command

```bash
git checkout -b feature-login
```

Creates and immediately switches to `feature-login`.

### List All Branches

```bash
git branch
```

Lists all local branches. Active branch is marked with `*`.

### Delete a Branch (Local)

```bash
git branch -d feature-login
```

Deletes the branch (only if merged). Use `-D` to force delete:

```bash
git branch -D feature-login
```

---

## 🌍 Remote Branches

### Push a Local Branch to Remote

```bash
git push origin feature-login
```

### Track a Remote Branch

```bash
git checkout --track origin/feature-login
```

### Delete a Remote Branch

```bash
git push origin --delete feature-login
```

---

## 🧪 Best Practices

- Name branches clearly: `feature/login`, `bugfix/navbar`, `hotfix/payment-error`
- Always branch off the latest `main`/`develop`
- Merge using Pull Requests (PRs) for collaboration
- Delete branches after merging

---

## 📘 Example Workflow

```bash
git checkout main
git pull origin main

# Create feature branch
git checkout -b feature/user-auth

# Work on code...
git add .
git commit -m "Add user authentication logic"

# Push branch to remote
git push origin feature/user-auth
```

---

> Branching helps you manage features, fixes, and experiments without interrupting other work. Mastering Git branches is essential for team collaboration and clean code management.

