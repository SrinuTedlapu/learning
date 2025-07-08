# 🌿 Git Branch - Detailed Notes

## 🔰 What is a Branch in Git?

A **branch** in Git is a lightweight movable pointer to a commit. Branches allow you to work on different versions of a project independently.

By default, Git creates a branch named `main` (or previously `master`). You can create new branches to experiment or develop features separately.

---

## 📜 Common Branch Commands

### ✅ View All Branches

```bash
git branch
```

- Shows local branches
- Current branch is marked with `*`

### 🌐 View Remote Branches

```bash
git branch -r
```

- Shows branches on remote repositories (like GitHub)

### 🌍 View Local + Remote Branches

```bash
git branch -a
```

---

### 🌱 Create a New Branch

```bash
git branch feature-branch
```

- Creates a new branch named `feature-branch`
- Stays on the current branch

### 🔀 Switch to a Branch

```bash
git checkout feature-branch
```

OR (recommended):

```bash
git switch feature-branch
```

### 🌿 Create and Switch (shortcut)

```bash
git checkout -b new-feature
```

OR

```bash
git switch -c new-feature
```

---

### ❌ Delete a Branch

```bash
git branch -d feature-branch     # Deletes only if fully merged
git branch -D feature-branch     # Force delete even if not merged
```

### 📤 Push Branch to Remote

```bash
git push origin feature-branch
```

### 🔁 Track Remote Branch Locally

```bash
git checkout -b feature origin/feature
```

---

## 🔍 Useful Tips

- Keep branch names short and meaningful: `fix-login`, `feature/signup-form`
- Regularly merge or rebase from `main` to keep your feature branches updated

---

## 🧪 Example

```bash
git checkout -b bugfix/error-page
# Work on the bug fix
git add .
git commit -m "Fix: error page not loading"
git push origin bugfix/error-page
```

---

## ✅ Summary

| Command                            | Description                         |
|------------------------------------|-------------------------------------|
| `git branch`                       | List branches                       |
| `git branch name`                  | Create a branch                     |
| `git checkout name`                | Switch to a branch                  |
| `git checkout -b name`             | Create and switch                   |
| `git branch -d name`               | Delete branch (safe)                |
| `git branch -D name`               | Force delete                        |
| `git push origin name`             | Push branch to remote               |

---

Happy branching! 🌿