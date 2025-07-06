
# Git Initialization

## What is Git Initialization?

Git initialization is the first step in starting version control for a project. When you initialize Git in a folder, it creates a `.git/` hidden directory, which allows Git to track changes in that folder.

---

## How to Initialize Git

### 🔹 Step 1: Open Terminal / Git Bash

Navigate to your project folder using the terminal or Git Bash:

```bash
cd path/to/your/project
```

### 🔹 Step 2: Initialize Git

Run the following command:

```bash
git init
```

This command:
- Creates a new subdirectory named `.git`
- Sets up the project as a Git repository
- Does not track files yet (you must add them manually)

---

## What Happens Internally?

When you run `git init`, it creates the following inside the `.git/` folder:
- `HEAD`: points to the current branch (default is `master` or `main`)
- `config`: repository-specific configuration
- `objects/`: stores all content (blobs, trees, commits)
- `refs/`: references to commit objects

---

## Example

```bash
mkdir myproject
cd myproject
git init
```

**Output:**
```
Initialized empty Git repository in /your/path/myproject/.git/
```

---

## After Initialization

You can start tracking files:

```bash
git add .
git commit -m "Initial commit"
```

---

## Check If a Folder is a Git Repo

To check if a folder is already a Git repo:

```bash
ls -a
```

If you see a `.git/` folder, it is a Git repository.

---

## Set Default Branch Name (Optional)

To set `main` as the default branch name globally:

```bash
git config --global init.defaultBranch main
```

Now when you run `git init`, it will start with `main` instead of `master`.

---

## Summary

| Command | Description |
|--------|-------------|
| `git init` | Initialize a new Git repository |
| `git config --global init.defaultBranch main` | Set default branch as `main` |
| `ls -a` | Check for `.git/` folder |

---
