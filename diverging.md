# Incase of Diverging remote and local

## Merging if its okay

```bash
git stash # saving current unstaged changes

git pull origin main # pull and merge remote changes

git stash pop # reapply local changes

git add . # or git add file_to_stage

git commit -m "commit message" # Should be eleborate on what you did

git push
```

## Rebase instead of merge(has a cleaner history)
- Has linear history(no merge commits)
- Avoids messy merge commits
- Reviews are easier

```bash
git stash

git pull --rebase origin main

git stash pop

git add . # or git add file_to_stage

git commit -m "commit message"

git push

```


