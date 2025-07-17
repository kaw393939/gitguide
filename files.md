Content:

# 📁 Managing Files in Git

Git helps you track every change you make to your files — but it's important to understand the different stages a file can be in and how to manage those changes effectively. This page covers the most important commands for adding, restoring, and inspecting file changes.

---

## 📄 `git status`

```bash
git status
````

**What it does:**
Displays the state of your working directory and staging area. It shows which files are untracked, modified, staged, or ready to commit.

**Narrative:**
You’ve been working on several files and can’t remember what you’ve changed. Running `git status` gives you a clear view of what’s changed and what Git is paying attention to.

---

## ➕ `git add`

```bash
git add <file>
git add .
```

**What it does:**
Stages one or more files, meaning you’re telling Git to include those changes in your next commit. `git add .` adds all modified or new files in the current directory.

**Narrative:**
You’ve completed a small feature or fixed a bug and want to save your work. You run `git add` to prepare just the relevant files for your commit, keeping your history focused and clean.

---

## 📝 `git commit -m`

```bash
git commit -m "Your descriptive message"
```

**What it does:**
Records a snapshot of the staged changes with a message describing what was done.

**Narrative:**
You’ve added a new function to your program. Committing the change creates a save point and leaves a note in the project history, making it easy to revisit or share your progress.

---

## 🔍 `git diff`

```bash
git diff
```

**What it does:**
Shows the changes between your working directory and the last commit — specifically the unstaged changes.

**Narrative:**
You want to double-check what you changed in a file before staging it. `git diff` gives you a line-by-line breakdown of exactly what was added, modified, or removed.

---

## 📑 `git diff --staged`

```bash
git diff --staged
```

**What it does:**
Shows the differences between the staged version of the file and the last commit.

**Narrative:**
You already ran `git add`, but want to verify what will go into your next commit. This command confirms exactly what's staged and ready to be saved.

---

## ♻️ `git restore`

```bash
git restore <file>
```

**What it does:**
Reverts a file in your working directory to match the last committed version, discarding any local changes.

**Narrative:**
You experimented with a file but decided your changes aren’t worth keeping. `git restore` lets you quickly undo all uncommitted edits and go back to the last saved version.

---

## ⬅️ `git checkout -- <file>` (older syntax)

```bash
git checkout -- <file>
```

**What it does:**
Same as `git restore`, but uses older syntax. Restores the file to its last committed state.

**Narrative:**
If you're using an older version of Git, this is how you'd discard unwanted local changes to a specific file.

---

## 📝 Tips for Students

* Use `git status` frequently to understand what’s happening in your repo.
* Stage only what’s relevant to the task at hand — this keeps your commit history useful.
* Use `git diff` before adding files, and `git diff --staged` before committing.
* Use `git restore` (or `checkout --`) to discard mistakes *before* they get committed.

