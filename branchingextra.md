### To see all the branches in local
```bash
git branch
```
### deleting a local branch if done with it
```bash
git branch -d branch-name
```

### To force delete(if trying something that did not work)
```bash
git branch -D branch-name
```

### In order to see the branches on remote
```bash
git branch -r
```

### To delete a remote branch
```bash
git push origin --delete branch-name
```

### cleaning up stale remote branches ..
If you have deleted branches on the remote but they still appear locally,
clean them up with:
```bash
git fetch --prune
```
The above is a Git command that cleans up references to remote branches that no longer exist on the remote.

When to use it:
-When cleaning up your local repo from old/stale branches
-Before running scripts or CI that rely on accurate list if remote branches

One can even configure git to always prune when fetching.

```bash
git config --global fetch.prune true
```