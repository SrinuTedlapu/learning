
# Basic Git Workflow

The basic Git workflow consists of a series of steps used to track and manage changes to a project. These steps ensure that your code is version-controlled and safely stored in a local or remote repository.

---

## 🔄 Git Workflow Overview

1. **Initialize a Git repository** (once per project)
2. **Track changes** using `git add`
3. **Save changes** using `git commit`
4. **Push to remote** repository (e.g., GitHub) using `git push`
5. **Update local copy** using `git pull`

---

## 1. Initialize Repository

```bash
git init
```

Initializes a new Git repository in the current directory by creating a `.git` folder.

---

## 2. Check Status

```bash
git status
```

Shows the status of files in the working directory. Helps you see:
- Modified files
- Untracked files
- Changes staged for commit

---

## 3. Stage Files (Add)

```bash
git add <filename>       # Add a specific file
git add .                # Add all files
```

Stages changes to be included in the next commit.

---

## 4. Commit Changes

```bash
git commit -m "Your commit message"
```

Records the staged changes in the local repository. Always write meaningful commit messages.

---

## 5. Connect to Remote Repository

```bash
git remote add origin <remote_repo_url>
```

Adds a remote repository (e.g., on GitHub) and names it `origin`.

---

## 6. Push to Remote

```bash
git push -u origin main
```

Sends your committed changes to the remote repository on the `main` branch.

---

## 7. Pull Changes from Remote

```bash
git pull origin main
```

Fetches and merges changes from the remote repository to your local branch.

---

## 🔁 Full Example Workflow

```bash
# Initialize a new Git repo
git init

# Track changes
git add .

# Commit changes
git commit -m "Initial commit"

# Connect to remote GitHub repository
git remote add origin https://github.com/user/repo.git

# Push to remote
git push -u origin main

# Pull latest changes
git pull origin main
```

---

## Summary Table

| Step       | Command                        | Description                            |
|------------|--------------------------------|----------------------------------------|
| Init       | `git init`                     | Start a new Git repository             |
| Track      | `git add .`                    | Stage all files for commit             |
| Commit     | `git commit -m "msg"`          | Save changes with a message            |
| Remote Add | `git remote add origin <url>`  | Link to a GitHub repo                  |
| Push       | `git push -u origin main`      | Upload commits to GitHub               |
| Pull       | `git pull origin main`         | Get updates from GitHub                |

---
