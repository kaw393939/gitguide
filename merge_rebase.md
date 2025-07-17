# 🔀 Merging and Rebasing in Git

Version control becomes especially powerful when you're working with **branches**. Two common ways to integrate changes from one branch into another are **merge** and **rebase**. Both have different workflows and use cases.

---

## 🌿 `git merge`

```bash
git merge <branch-name>
````

**What it does:**
Combines the history of the specified branch into your current branch, creating a new "merge commit" to capture the integration.

**Narrative:**
You’ve been working on a feature in a branch called `feature/login`. Once it's tested and ready, you switch back to `main` and run `git merge feature/login` to bring in your changes. This preserves the full history of both branches and shows when they came together.

**Example:**

```bash
git checkout main
git merge feature/login
```

---

## 🔄 `git rebase`

```bash
git rebase <branch-name>
```

**What it does:**
Moves or "replays" your branch’s commits on top of another branch, rewriting the commit history to appear as if your work started from the tip of that branch.

**Narrative:**
You’ve made several commits in `feature/ui-update`, but meanwhile, new commits were added to `main`. You run `git rebase main` to replay your work on top of the latest version of `main`, resulting in a cleaner, linear history. This is especially useful for keeping your project tidy before pushing to a shared repository.

**Example:**

```bash
git checkout feature/ui-update
git rebase main
```

---

## ⚖️ Merge vs. Rebase Summary

| Feature      | `git merge`                        | `git rebase`                            |
| ------------ | ---------------------------------- | --------------------------------------- |
| History      | Keeps full branching history       | Rewrites history to be linear           |
| Commit style | Creates a merge commit             | Rewrites commits                        |
| Use when…    | You want to preserve collaboration | You want a clean, linear history        |
| Risk         | Low                                | Can be risky if done on shared branches |

---

## 📝 Tip for Students

If you're working with a team, **prefer `merge`** for integrating shared branches. Use `rebase` for cleaning up your personal branches **before merging or pushing**, especially to avoid cluttered commit logs in pull requests.
