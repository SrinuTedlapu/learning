# 🔀 Git Merging - Detailed Guide

Merging in Git allows you to combine changes from one branch into another. This is crucial when working in teams or developing features in isolation.

---

## 📌 What is a Merge?

A **merge** brings the history and content of one branch into another. Most often, you merge a feature branch into `main` or `develop`.

---

## 🔁 Types of Merges

### 1. **Fast-forward Merge**
Occurs when the current branch has no new commits since it branched off. Git simply moves the pointer forward.

```bash
git checkout main
git merge feature-login
```

If `main` hasn’t changed since `feature-login` was created, the merge will fast-forward.

### 2. **3-Way Merge**
Occurs when both branches have unique commits. Git creates a new commit that combines both histories.

```bash
git checkout main
git merge feature-login
```

Git will auto-merge the changes and prompt for a commit if necessary.

---

## ⚠️ Merge Conflicts

Conflicts happen when the same parts of a file are modified differently in two branches. Git cannot decide which change to keep.

### Example Conflict Message
```
CONFLICT (content): Merge conflict in app.js
Automatic merge failed; fix conflicts and then commit the result.
```

### How to Resolve a Conflict
1. Open the conflicted file:
   ```
<<<<<<< HEAD
Your changes
=======
Other branch changes
>>>>>>> feature-login
   ```
2. Edit the file to keep the desired content.
3. Stage the resolved file:
   ```bash
   git add app.js
   ```
4. Commit the merge:
   ```bash
   git commit
   ```

---

## 📘 Common Merge Commands

### Merge a Branch into Current Branch
```bash
git merge feature-login
```

### Abort a Merge (if conflicts are too complex)
```bash
git merge --abort
```

### Continue After Manual Conflict Resolution
```bash
git add <resolved-files>
git commit
```

---

## 🧪 Best Practices
- Always pull the latest changes before merging:
  ```bash
  git pull origin main
  ```
- Communicate with teammates before merging shared code.
- Clean up old feature branches after merging.

---

## ✅ Merge vs Rebase (Quick Note)
- **Merge**: Keeps the history of both branches.
- **Rebase**: Rewrites history as if work happened sequentially.

Use merge for collaboration and rebase for a cleaner linear history.

---

## 🧪 Example Workflow
```bash
git checkout main
git pull origin main

git checkout feature/login
# Make changes
# Commit changes
git push origin feature/login

git checkout main
git merge feature/login
# Resolve conflicts if any
git push origin main
```

---

> Merging is essential for collaborative development. Understanding how to resolve conflicts and maintain a clean history makes your Git workflow smoother and more professional.

