## git reset mixed
```bash
git reset --mixed HEAD-1
```

### What it does:
This moves the HEAD pointer to a specific commit, keeps both working directory , but unstages all changes

### Narrative:
The default for reset if you don't specify which version you want. Great for re-editing/regrouping changes
before doing another commit.