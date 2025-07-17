# 📦 Git Stash Guide

Sometimes you're in the middle of working on something, but you need to switch tasks or fix a bug — and your current changes aren't ready to be committed yet. That's where `git stash` comes in.

---

## 📥 `git stash`

```bash
git stash
````

**What it does:**
Temporarily saves (or "stashes") your uncommitted changes and reverts your working directory to match the latest commit. This lets you switch branches or work on something else without losing your current progress.

**Narrative:**
You’re halfway through building a feature when your professor or team lead asks you to fix a bug on the `main` branch. Your changes aren’t ready to commit yet, so you use `git stash` to set them aside, switch to `main`, fix the bug, and come back later to finish what you were doing.

---

## 📤 `git stash pop`

```bash
git stash pop
```

**What it does:**
Restores your most recent stashed changes and removes them from the stash list.

**Narrative:**
After fixing the urgent issue, you're ready to resume where you left off. You run `git stash pop` to bring your stashed work back into your working directory, right where you left it.

---

## 🧠 Bonus Tips

* You can view a list of all stashes:

  ```bash
  git stash list
  ```

* You can apply a stash without removing it:

  ```bash
  git stash apply
  ```

* You can stash changes to specific files only:

  ```bash
  git stash push <file1> <file2>
  ```

---

## 📝 Tip for Students

Use `git stash` when you're mid-task and don’t want to commit unfinished work just to switch branches. It helps keep your commits clean and lets you multitask like a pro.
