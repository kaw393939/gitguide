# 🧠 Git Tips, Tricks, and Common Fixes As you get more comfortable with Git, you'll encounter situations that require a bit more skill. This guide provides practical tips, advanced commands, and fixes for common problems students face when working with Git. 🧼 1. Cleaning Up Mistakes ❌ Undoing the Last Commit (But Keeping the Changes) git reset --soft HEAD~1

**Use case:**  
You made a commit but forgot to include a file or write a good message. This lets you redo it without losing your work.

- - -

### ❌ Undoing the Last Commit AND Unstaging the Files

```bash
git reset --mixed HEAD~1
```

**Use case:**  
You committed and now realize the changes shouldn’t be staged or committed yet. This resets the index but keeps the files.

- - -

### 🔥 Throw Away the Last Commit and All Changes

```bash
git reset --hard HEAD~1
```

**Use with caution!**  
This will erase your last commit _and_ all uncommitted changes in your working directory. Make sure you **really** want to do this.

- - -

## 🧭 2. Navigating Your History

### 🔍 Show History in a Pretty Graph

```bash
git log --oneline --graph --all
```

**Use case:**  
Great for visualizing branch and merge history.

- - -

### 🧳 View a Specific Commit

```bash
git show <commit-hash>
```

**Use case:**  
Useful for reviewing what happened in a commit before cherry-picking or reverting it.

- - -

## 🧵 3. Fixing Merge Conflicts

### 🧶 Common Steps

1.  Try to merge or rebase.
    
2.  Git will mark conflicts in the affected files.
    
3.  Manually edit the files to fix the conflicts.
    
4.  Mark as resolved and commit:
    

```bash
git add <fixed-file>
git commit
```

### 🧠 Pro Tip:

Use a visual merge tool like VS Code or a Git GUI (GitHub Desktop, SourceTree) to resolve conflicts more easily.

- - -

## 🎯 4. Rewriting Commit History

### 📝 Change the Last Commit Message

```bash
git commit --amend -m "Better commit message"
```

**Use case:**  
You mistyped your last commit message or want to clarify it.

- - -

### 🪄 Interactive Rebase (Advanced)

```bash
git rebase -i HEAD~3
```

**Use case:**  
You want to clean up the last 3 commits (reorder, squash, rename, delete).

- - -

## 🧳 5. Move Changes Between Branches

### 🍒 Cherry Pick a Commit

```bash
git cherry-pick <commit-hash>
```

**Use case:**  
You fixed a bug on one branch and want to apply that same fix to another branch without merging everything.

- - -

## 💡 6. Miscellaneous Pro Tips

*   🛡️ **Always pull before pushing** to avoid merge conflicts.
    
    ```bash
    git pull origin main
    ```
    
*   🔍 **Search commit history for a string**
    
    ```bash
    git log -S"someFunctionName"
    ```
    
*   🔍 **Find who last modified a line**
    
    ```bash
    git blame <file>
    ```
    
*   🧹 **Remove untracked files and folders**
    
    ```bash
    git clean -fd
    ```
    
*   🧪 **Temporarily try changes without committing**
    
    ```bash
    git stash
    git stash pop
    ```
    

- - -

## 🛠️ 7. Common Student Problems (And Fixes)

Problem | Solution -- | -- “I committed to the wrong branch” | git checkout main → git cherry-pick the commit OR rebase “I deleted a file accidentally” | git checkout HEAD OR git restore “Merge conflict nightmare” | Use a visual diff tool (VS Code), take it slow, and commit resolved changes “I pushed something I shouldn’t have” | If it's sensitive, contact your instructor; otherwise, you may use git revert or git reset (if safe) “My repo is totally broken” | Clone it fresh into a new folder and reapply your work. It’s OK to start clean.

- - -

## 🏁 Final Advice

*   🔄 **Commit often** — small, meaningful commits are easier to debug and review.
    
*   🔍 **Always read what `git status` tells you.**
    
*   💬 **Ask for help early** — Git problems don’t fix themselves.
    
*   📚 Keep a personal copy of this guide for reference.
    

- - -