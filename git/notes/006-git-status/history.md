
# Git Status and History

Understanding the status and history of your repository is crucial when working with Git. These commands help you keep track of file changes and the commit timeline.

---

## 🔍 1. git status

### ✅ Purpose:
Shows the current state of the working directory and staging area.

### 📌 What It Tells You:
- Which files are staged for the next commit
- Which files are modified but not staged
- Which files are untracked (new files)

### 🧪 Example:

```bash
git status
```

### 📤 Output Example:
```
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
        modified:   index.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        script.js
```

### 🧠 Notes:
- Helps avoid mistakes by checking what will be committed
- Encourages clean, understandable commit stages

---

## 🕓 2. git log

### ✅ Purpose:
Displays the commit history for the repository.

### 📌 Shows:
- Commit ID (SHA hash)
- Author
- Date & time
- Commit message

### 🧪 Example:

```bash
git log
```

### 📤 Output Example:
```
commit a1b2c3d4e5f6g7h8i9j0
Author: Your Name <you@example.com>
Date:   Sun Jul 6 19:00:00 2025 +0530

    Add homepage layout

commit 0123456789abcdef
Author: Your Name <you@example.com>
Date:   Sat Jul 5 17:00:00 2025 +0530

    Initial commit
```

### 🧠 Tips:
- Use `q` to exit the log viewer
- Press arrow keys to scroll

---

## 🧾 Extra: Custom Log Output

```bash
git log --oneline
```

Gives a short, one-line summary per commit.

Example:
```
a1b2c3d Add homepage layout
0123456 Initial commit
```

---

## 🧾 Extra: Show Specific Commit

```bash
git show <commit_id>
```

Displays detailed changes made in a specific commit.

---

## ✅ Summary Table

| Command                  | Description                           |
|--------------------------|---------------------------------------|
| `git status`             | Show working directory & staged files |
| `git log`                | Show full commit history              |
| `git log --oneline`      | Show summarized commit history        |
| `git show <commit_id>`   | Show detailed changes for a commit    |

---
