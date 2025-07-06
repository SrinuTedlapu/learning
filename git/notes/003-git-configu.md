# 🟢 Step 3: Git Configuration

Once Git is installed, it’s important to set up your identity and preferred defaults.

---

## ✅ 1. Configure User Identity (Required)

This is used to label your commits:

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

The `--global` flag means it applies to all repositories on your computer.

You can override it per project (locally):

```bash
git config user.name "Project-Specific Name"
git config user.email "project@email.com"
```

---

## ✅ 2. Check Configuration

```bash
git config --list
```

You’ll see entries like:

```
user.name=Your Name
user.email=your@email.com
core.editor=code --wait
```

---

## ✅ 3. Set Default Editor (Optional)

To set VS Code as your default Git editor:

```bash
git config --global core.editor "code --wait"
```

Or use nano (Linux default):

```bash
git config --global core.editor nano
```

---

## ✅ 4. Set Default Branch Name (Recommended)

By default, Git might name the first branch `master`. You can change the default to `main`:

```bash
git config --global init.defaultBranch main
```

---

## ✅ 5. Useful Optional Configs

| Setting                       | Command Example                                     |
| ----------------------------- | --------------------------------------------------- |
| Show colored output           | `git config --global color.ui auto`                 |
| Enable credential caching     | `git config --global credential.helper cache`       |
| Enable helpful status display | `git config --global status.showUntrackedFiles all` |

---

## ✅ 6. View All Settings by Scope

### Global (user-wide):

```bash
git config --global --list
```

### Local (per repo):

```bash
git config --local --list
```

### System (machine-wide):

```bash
git config --system --list
```

---

## ✅ What’s Next?

- Learn how to **create and initialize a Git repository**
- Practice `git init`, `git add`, `git commit`, `git status`

Go to 👉 **Step 4: Create a Git Repository**
