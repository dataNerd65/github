# github
For github use

-- colections of all github concepts I use
### collaborating well and effectively
we clone the repository creating a copy of it on my machine
```bash
git clone https://github.com/username/repository-name.git #this is the link to remote
cd repository-name
```
then we branch from main to another branch we create
```bash
git checkout -b feature-branch-name # small features per branch eg "add-login-page"
# The branch will be switched from main to this branch we have created.

```
then we push the branch to remote for tracking
```bash
git push -u origin feature-branch-name

```

make some changes on that branch then do the necessary
```bash
git status

git add . # or git add filenamechanged

git commit -m "Added a login form" # message saying what you did
 
# then push
git push origin feature-branch-name # good so you specify well

# Also this is acceptable

git push

```
Once your changes are pushed, you need to create a pull request so others can review and merge your changes.


1. **Go to GitHub (or your Git hosting platform)** and navigate to your repository.
2. You'll often see a banner prompting you to create a pull request for the branch you just pushed. Click on **"Compare & pull request"**.
3. Add a **title** and **description** of the changes in the PR form.
4. Select the branch you want to merge your changes into (usually `main` or `develop`).
5. **Submit the pull request** for review.

### **Code Review and Discussion**

Once the pull request is created, your team members will be able to:

- **Review the code**: They will leave comments, feedback, or approve the changes.
- **Request changes**: If there are issues with your code, they might request changes. You can continue working on the same branch to fix any issues.

### **Resolve Merge Conflicts (if any)**

If there are conflicting changes between your branch and the base branch (usually `main`), you'll need to resolve them before your pull request can be merged.

**Pull the latest changes from the base branch (e.g., `main`)**:

```bash
git checkout main # also git switch main can be used
git pull origin main # git pull also works if you are in the branch you want to pull to
# but explicitly saying the branch name is good
```

Switch back to your feature-branch
```bash
git checkout feature-branch-name # still git switch feature-branch-name
```

merge the latest `main` changes into your branch
```bash
git merge main
```
**Resolve any conflicts** manually in the affected files. Git will mark the conflicts, and you'll need to decide how to merge them.

**Stage and commit the resolved files**:
```bash
git add conflicted-file
git commit -m "Resolved Merge Commit"
```
**Push the updated branch**
```bash
git push origin feature-branch-name
```
### Merge the Pull Request**

After your pull request is approved and all conflicts are resolved, it’s time to merge it into the main branch.

1. If you're the one handling the PR, you can merge it yourself by clicking the **"Merge pull request"** button on GitHub.
2. If someone else is reviewing, they will merge it once they approve.

Once the PR is merged, you can **delete your feature branch** both locally and remotely to keep the repository clean:

Delete locally

```bash
git branch -b feature-branch-name
```
Deleting remotely
```bash
git push origin --delete feature-branch-name
```
Pull regularly before anything