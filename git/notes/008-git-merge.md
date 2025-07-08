# 🔀 Git Merge - Detailed Notes

## 🔰 What is Git Merge?

`git merge` is used to **combine the changes** from one branch into another. Typically, you merge a **feature branch** into the **main** or **development** branch.

---

## 🧠 How Merging Works

When you merge one branch into another, Git:
- Identifies the **common ancestor** commit
- Applies the changes made in the other branch **on top** of the current branch

---

## 🔀 Basic Merge Syntax

```bash
git checkout main
git merge feature-branch
```

- This merges `feature-branch` into `main`
- You must be on the **target** branch (usually `main`) before merging

---

## ✅ Fast-forward Merge

Occurs when no new commits exist on the target branch since it diverged. Git simply moves the pointer forward.

```bash
git merge feature-branch
# No merge commit is created
```

---

## 🧩 3-Way Merge (with a merge commit)

Happens when both branches have made changes. Git creates a **merge commit** to record the merge.

```bash
git merge feature-branch
# Creates a merge commit like "Merge branch 'feature-branch'"
```

---

## ⚠️ Merge Conflicts

If Git cannot automatically merge, it will show a **conflict**.

Steps to resolve:

```bash
# 1. Open conflicted files and fix them manually
# 2. Stage the resolved files
git add <file>

# 3. Continue the merge
git commit
```

---

## 🧹 Abort a Merge

If you want to cancel an in-progress merge:

```bash
git merge --abort
```

---

## 📤 Pushing a Merged Branch

After a merge is complete:

```bash
git push origin main
```

---

## 📘 Example Workflow

```bash
git checkout -b feature/login
# Work and commit on feature/login branch

git checkout main
git pull origin main         # Make sure main is up to date
git merge feature/login      # Merge the feature branch into main
git push origin main         # Push the updated main to GitHub
```

---

## 📝 Summary of Key Commands

| Command                      | Description                                  |
|-----------------------------|----------------------------------------------|
| `git merge branch-name`     | Merge into current branch                    |
| `git merge --abort`         | Abort ongoing merge                          |
| `git pull --rebase`         | Preferred when collaborating (avoids merge commits) |
| `git push`                  | Push merged result to remote                 |

---

## ✅ Best Practices

- Always **pull the latest changes** before merging
- Resolve conflicts carefully
- Delete merged branches if no longer needed

---

Happy merging! 🔀